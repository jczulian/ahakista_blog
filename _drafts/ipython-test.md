---
layout: post
title:  "IPython test"
date:   2013-11-01
categories: 
---


# How to write a laptop battery monitor in Python

This is a short tutorial on how to write a battery monitor in python.

The goal is to learn some python and some of its libraries. We will use Gtk
python binding in order to show a nice icon in the system tray that informs the
user about the battery status. We will also have to craft some regular
expression in order to extract information from data contained in textual
format. We will also have to find out how to run system commands and get their
output.

## Running system command from Python and retrieving its output

The first thing we must do in order to run system command from python is to use
the subprocess module.


    import subprocess




    0



The call function will spawn a new process and run the command given as the
first array element. This function only returns the exit code of the process. So
you will only know if the process has ran without error or if it encounter
problems.


    subprocess.call(["ls", "-l"])




    0



The check_output function is more interesting for us. It does basically the same
thing as the 'call' function but it returns the output of the command once this
one has terminated.


    subprocess.check_output(['ls', '-l', '/home/'])




    'total 12\ndrwxr-xr-x 134 jc jc 12288 Nov  1 14:20 jc\n'




    
