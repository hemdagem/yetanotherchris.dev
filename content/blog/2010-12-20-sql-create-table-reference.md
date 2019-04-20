---
title: SQL create table reference
date: 2010-12-20 00:00:00 Z
permalink: "/sql-server/sql-create-table-reference/"
tags:
- sql-server
Published: 2010-12-20 00:00:00 Z
author: Chris S
layout: post
dsq_thread_id:
- 1085023075
---

Here's a quick reference for scripting table creation in SQL server by hand, where the text is readable and pretty rather than an autogenerated mess.

<!--more-->

  
`gist:yetanotherchris/4960139`

It's usually easier to bulk add the foreign keys after, that way the order of the CREATE TABLES doesn't matter:

<pre>ALTER TABLE [dbo].[sometable] ADD CONSTRAINT [FK_sometable_users_id] 
	FOREIGN KEY([userid]) REFERENCES [dbo].[users] ([id])
</pre>