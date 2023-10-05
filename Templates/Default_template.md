<%*
  let title = tp.file.title
  if (title.startsWith("Untitled")) {
    title = await tp.system.prompt("Title");
    await tp.file.rename(title);
  }
   tags = await tp.system.prompt("Tags")
%>---
aliases: [ "<%tp.file.creation_date("YYYYMMDDHHmmss") %>",  ]
tags: <%* tR += tags %>
date_created: <% tp.file.creation_date() %>
---
# <%* tR += title %>
---
