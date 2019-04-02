---
title: "Hosting a remote development server"
layout: post
date: 2019-03-16 10:00
image: /assets/images/markdown.jpg
headerImage: false
tag:
- vscode
- code-server
- remote-development
category: blog
author: gandhar
description: Run VS Code on a remote server
---

## Intent

We'll be using [code-server](https://github.com/codercom/code-server), a great initiative by [Coder](https://coder.com/) in making the process of self hosting a remote development environment serving [Visual Studio Code](https://code.visualstudio.com/) easy.

You'll learn how you can host a remote working environment for your project in minutes.

## The Why?

Before going ahead the first question everyone will be asking would be "Why would I need a remote code editor for my project?". Well to quote [code-server](https://github.com/codercom/code-server)

> * Code on your Chromebook, tablet, and laptop with a consistent dev environment.
> 	* If you have a Windows or Mac workstation, more easily develop for Linux.
> * Take advantage of large cloud servers to speed up tests, compilations, downloads, and more.
> * Preserve battery life when you're on the go.
>	* All intensive computation runs on your server.
>	* You're no longer running excess instances of Chrome.

To simplify, we can harness the processing power of remote machine to run tests and builds without sacrificing performance of your local machine.

## Requirements

- Account on any cloud hosting service like AWS, Azure, GCP
- Nginx for serving platform on the Web

For this exercise purpose we'll we using AWS and because I don't use any other service 😂

- Boot a new instance with `Ubuntu Server 18.04 LTS`. You can choose any instance of your choice e.g. `t2.micro`
- Make sure you keep port 80 open on this instance, you can open 443 as well for SSL connection.