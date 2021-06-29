---
ID: 176
post_title: >
  How to use Hiren Boot CD programs with
  switches
post_name: >
  notron-ghost-switches-hiren-bootcd-application-switches-command-prompt
author: ku1deep
post_date: 2010-07-02 10:20:24
layout: post
link: >
  http://revolutioners.com/notron-ghost-switches-hiren-bootcd-application-switches-command-prompt/
published: true
tags:
  - internet
  - technology
  - tricks
categories:
  - Personal
---
Last night it look me over 3 hours to understand the problem why Norton Ghost was acting weird. I was not able to clone my laptop hard drive with an existing image. The image was correct and consistent however Norton Ghost while restoring kept giving me some inconsistency errors. Image was created with a 160 GB partition and I was restoring it on 320 GB drive. I tried both ways to restore. Image to Drive and Image to Disk. But every time it gave me inconsistency errors.
<span id="more-2028"></span>

Finally after some research I found out the solution for the problem. There are various switches that you can use on command line Ghost. I had to use <strong>-ntc-</strong> switch. This switch basically Disables NTFS contiguous run allocation which makes the image to be restored on any hard drive with any size of drive. But unfortunately when you use Hiren Bootcd you can not run Ghost with any switch.

But suddenly all my problems were solved. Actually what happens is whenever you run any program from the menu it first gets extracted and then gets saved in the RAM drive created by the CD. That’s it. That was the solution.

To run Ghost or any other program from Hiren Bootcd with switches follow the steps below:
<ol>
 	<li>Boot with Hiren BootCD.</li>
 	<li>Run a program of your choice. I was using Ghost so I will continue with Ghost with the example.</li>
 	<li>Once Ghost is up and running <strong>Exi</strong>t it without doing anything.</li>
 	<li>It will take you back to the Command Prompt.</li>
 	<li>Now use <strong>Ghost.exe -ntc-</strong></li>
 	<li>That’s it. Similarily you can use any program with their compatible switches. All you need to do is run it first and then exit it.</li>
</ol>
Pretty Simple huh !!