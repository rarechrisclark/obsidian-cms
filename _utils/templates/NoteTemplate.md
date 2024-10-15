<%*
  let title = tp.file.title;
  
  // If the file is untitled, prompt for a title
  if (title.startsWith("Untitled")) {
  title = await tp.system.prompt("What is the note title?");
  }
  
  // Extract the blog post name from the title and format it
  const noteSlug = title.replace(/ /g, "-").toLowerCase();
  
  // Rename the file to note-slug
  const newFileName = `${noteSlug}`;
  await tp.file.rename(newFileName);
  
  // Format the title to capitalise the first letter of each word
  const noteTitle = title
  .split(" ")
  .map(word => word.charAt(0).toUpperCase() + word.slice(1).toLowerCase())
  .join(" ");

  // Prompt for description input
  const noteDescription = await tp.system.prompt("Enter a brief description for the note");
  
  tR += "---";
%>
title: <%* tR += noteTitle %>
description: <%* tR += noteDescription %>
date: <% tp.file.creation_date("YYYY-MM-DD") %>
---
# <%* tR += noteTitle %>

%% Content here %%
