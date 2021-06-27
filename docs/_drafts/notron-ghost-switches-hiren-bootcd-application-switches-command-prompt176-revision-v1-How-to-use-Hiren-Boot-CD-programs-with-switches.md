---
id: 560
title: How to use Hiren Boot CD programs with switches
date: 2018-10-30T17:14:43+00:00
author: nimda
layout: revision
guid: https://revolutioners.com/176-revision-v1/
permalink: /?p=560
---
Last night it look me over 3 hours to understand the problem why Norton Ghost was acting weird. I was not able to clone my laptop hard drive with an existing image. The image was correct and consistent however Norton Ghost while restoring kept giving me some inconsistency errors. Image was created with a 160 GB partition and I was restoring it on 320 GB drive. I tried both ways to restore. Image to Drive and Image to Disk. But every time it gave me inconsistency errors.  
<span id="more-2028"></span>

Finally after some research I found out the solution for the problem. There are various switches that you can use on command line Ghost. I had to use **-ntc-** switch. This switch basically Disables NTFS contiguous run allocation which makes the image to be restored on any hard drive with any size of drive. But unfortunately when you use Hiren Bootcd you can not run Ghost with any switch.

But suddenly all my problems were solved. Actually what happens is whenever you run any program from the menu it first gets extracted and then gets saved in the RAM drive created by the CD. That’s it. That was the solution.

To run Ghost or any other program from Hiren Bootcd with switches follow the steps below:

  1. Boot with Hiren BootCD.
  2. Run a program of your choice. I was using Ghost so I will continue with Ghost with the example.
  3. Once Ghost is up and running **Exi**t it without doing anything.
  4. It will take you back to the Command Prompt.
  5. Now use **Ghost.exe -ntc-**
  6. That’s it. Similarily you can use any program with their compatible switches. All you need to do is run it first and then exit it.

Pretty Simple huh !!