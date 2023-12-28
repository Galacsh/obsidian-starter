---
<%-*
    let title = tp.file.title;
    if (title == null || title === "" || title.startsWith("Untitled")) {
        while (true) {
            try {
                title = await tp.system.prompt("Title", null, true, false);
                if (title === "") throw "Title cannot be empty";
                break;
            } catch (ignore) {}
        }
        await tp.file.rename(title);
    }

    /*
    let slug = title
        .toLowerCase()
        .trim()
        .replace(/[^\w\s-]/g, '')
        .replace(/[\s_-]+/g, '-')
        .replace(/^-+|-+$/g, '');
    */
%>
title: "<% title %>"
description: "TODO"
lastUpdated: <% tp.date.now('YYYY-MM-DD HH:mm:ss') %>
publish: false
---

==**Did you wrote description?**==<% tp.file.cursor() %>
