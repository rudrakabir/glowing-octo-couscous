# Templater Test

Current date: <% tp.date.now() %>

Formatted date: <% tp.date.now("dddd, MMMM Do YYYY") %>

File name: <% tp.file.title %>

File creation date: <% tp.file.creation_date("YYYY-MM-DD HH:mm:ss") %>

Yesterday: <% tp.date.yesterday("YYYY-MM-DD") %>

Tomorrow: <% tp.date.tomorrow("YYYY-MM-DD") %>

Random number between 1 and 100: <% Math.floor(Math.random() * 100) + 1 %>
