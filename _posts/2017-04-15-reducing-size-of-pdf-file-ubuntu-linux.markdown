---
layout: post
title:  "Reducing the size of a pdf file in Ubuntu/Linux"
date:   2017-04-15 15:06:18 -0400
categories: commandline
---
I recently faced a problem when I had to reduce the size of a PDF to comply with an online submission portal. This turned out to be a nightmarish scenario as I could not find a simple utility that does well for my file. Adobe Acrobat does, but probably an overkill to buy it just for this task.

So here's a trick that works. Using good old ghostscript:


{% highlight bash %}
# Install gs using your favorite package manager
sudo apt-get install ghostscript
 gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/screen -dNOPAUSE -dQUIET -dBATCH -sOutputFile=output.pdf input.pdf
{% endhighlight %}

Worked beautifully and saved me 20%, without any noticeable reduction in quality. Best part is that you can run this repeatedly, until you find the right tradeoff between size and quality.

If you want slightly higher quality, replace -dPDFsettings=/screen with either /ebook or /prepress.

Source: [Ask Ubuntu][ask-ubuntu-link]

[ask-ubuntu-link]: https://askubuntu.com/questions/113544/how-can-i-reduce-the-file-size-of-a-scanned-pdf-file/256449
