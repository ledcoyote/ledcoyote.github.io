---
layout: post
title: Linux Boxes All the Way Down?
tags: technology
permalink: /blog/linux-boxes-all-the-way-down.html
author: ellie
---

# Linux Boxes All the Way Down?

I've been working in technology for it seems like forever. I was putting
together PCs as a middle/high schooler, and I've installed my share of linux on
things—let's just say I'm comfortable with technology. I sort of missed the move
of _absolutely everything_ into the cloud in the late 2000s and 2010s, as I was
ensconced in mostly hardware-based work throughout this period. I only really
began my career as a professional programmer in 2019.

When I began in this industry I was working on a microservice-based web
application running on AWS. I started out on the frontend and got comfortable
fiddling with the dom and stylesheets. The backend was sort of a mystery. I knew
that we ran on virtual machines or something, and I heard of things like
databases and Kubernetes and other weird creatures that backed everything up.

Over time, I got more familiar with things that go on in the application backend
on the servers. However, even then I tended to think of all those cloud
components as abstract things—that they really were the vector graphic pictures
you see in architecture diagrams. It was only recently that I have started to
mess around with the pieces of software that make up those components. And I
realized: they are all just pieces of software running on Linux boxes!

You have something like RDS (AWS's Relational Database Service), and it is just
a PostgreSQL or MySQL program running on a Linux host with an SSD/HDD. The same
goes for Kubernetes or S3 or Jenkins or anything. All just software running on
machines (although I do know there's some fancyness going on with hypervisors
and packing multiple virtual machines onto a single physical box).

It was somewhat of an embarrassing realization when I had it (but also kind of a
["today's lucky 10,000"](https://xkcd.com/1053/) moment). However, it is
understandable when you think about _how much effort_ cloud providers have put
into _creating abstractions_ of these pieces of software running on Linux boxes,
so you don't have to worry as much about running the software. You can begin to
think of them as vector graphic icons in an architecture diagram. This is very
powerful, however I think it's good to take stock of the fact that it is only
slightly more complicated than simple programs running on Linux boxes. It's less
magical and scary to realize that—also empowering. I would invite you to take a
few steps further...

_Think_ of the actual physical hardware these programs are running on. They are
made of metal and glass, and they live inside big air-conditioned buildings.
_Think_ of the workers running around swapping hardware when it fails, and the
energy it takes to keep them and all that machinery cool and happy. _Think_ of
the delivery driver shuttling hardware to that building, of the worker in a
factory across the ocean assembling the server, of the potential that the
minerals used to forge the components was mined by children in a conflict
region. _Think_ of the carbon spewed into the atmosphere to power the whole
supply chain that delivers an emoji to your customer's web browser when they
click into your application.

It's Linux boxes, but that's only partway down. The whole enterprise is held
aloft by the efforts, some well-paid but the greater many not, of human workers,
and energy and minerals extracted from this Earth.
