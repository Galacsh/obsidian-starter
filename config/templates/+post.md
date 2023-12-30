---
<%-*
  let title = tp.file.title;
  while (true) {
    try {
      title = await tp.system.prompt("Title", title, true, false);
      if (title == null || title === "" || title.startsWith("Untitled")) {
        throw "Title cannot be empty";
      }
      break;
    } catch (ignore) {}
  }
%>
title: "<% title %>"
description: "TODO"
lastUpdated: <% tp.date.now('YYYY-MM-DD HH:mm:ss') %>
publish: false
---

> [!NOTE]
> Did you wrote description?  
> File name should be easy to sluggify.

<% tp.file.cursor() %>
