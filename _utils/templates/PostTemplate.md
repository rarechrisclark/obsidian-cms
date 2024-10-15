<%*
  let title = tp.file.title;
  
  // If the file is untitled, prompt for a title first
  if (title.startsWith("Untitled")) {
  title = await tp.system.prompt("What is the post title ");
  }
  
  // Extract the post post name from the title and format it
  const postSlug = title.replace(/ /g, "-").toLowerCase();
  
  // Rename the file to post-slug only after getting the title
  const newFileName = `${postSlug}`;
  await tp.file.rename(newFileName);
  
  // Format the title to capitalize the first letter of each word
  const postTitle = title
  .split(" ")
  .map(word => word.charAt(0).toUpperCase() + word.slice(1).toLowerCase())
  .join(" ");
  
  // Prompt for description input
  const postDescription = await tp.system.prompt("Enter a brief description for the post");
  
  tR += "---";
%>
title: <%* tR += postTitle %>
description: <%* tR += postDescription %>
date: <% tp.file.creation_date("YYYY-MM-DD") %>
---
# <%* tR += postTitle %>

%% Content here %%
