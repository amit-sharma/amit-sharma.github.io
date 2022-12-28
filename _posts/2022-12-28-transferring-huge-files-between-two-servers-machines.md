---
layout: post
title:  "Transferring HUGE files between two servers or remote machines"
date:   2012-12-28 10:06:18 -0400
categories: commandline
---
I wanted to transfer a 200GB file from one remote machine to another. This is 2022, so I thought it should be a breeze. But scp showed me ETA of 2 days! I looked frantically for solutions online. People suggested rcp (which gave the same speed) and then variants of it that did not use encryption. All of those options are disabled by new versions of OpenSSH. 

Others suggested using netcat, which is quite a nifty solution and it does not use encryption. Sharing the details here. The idea is to open a port on the receiving machine and then pipe your data into that port from the sending machine. 

{% highlight bash %}
# on the receiving machine (with network name REC-MACHINE)
nc -l 2022 > newfile.txt  # 2022 is the port number
{% endhighlight %}

{% highlight bash %}
# on the sending machine
nc REC-MACHINE 2022 < file-to-be-transferred.txt
{% endhighlight %}


But this was slow too. It seemed that the network between these two machines is slow. 

Other people suggested NFS, essentially mounting the remote folder as a drive on your host machine and then doing the transfer. I did not try it since it seemed like a lot of work. 

But then I realized most of the stackoverflow/serverfault questions were more than 4-5 years old. Wait, what was going on? Did no one had this problem in 2022? I searched some more, tried some more, and ended up wasting a lot of time.

The next morning I recalled coming across a tool called [rclone](https://rclone.org/). It was for cloud transfer and I initially thought that's not relevant. But it turns out that transferring a file to a cloud service provider from the sending machine, and then downloading the file from the cloud storage to the receiving machine, is way faster than transferring it directly. Woah!

Cloud storage providers have optimized file transfers and also have servers availability across the world. So in 2022, the best solution to transfer HUGE files is to use cloud storage like Dropbox. rclone is quite easy to use. Here are the steps needed. 

{% highlight bash %}
# on the sending machine
# setup a cloud storage provider (called myremote)
# (can be done on a headless server too)
rclone config 
rclone copy file-to-be-transferred.txt myremote:folder-path/ --progress --stats-one-line
{% endhighlight %}

[Source: rclone.org](https://rclone.org/dropbox/)
