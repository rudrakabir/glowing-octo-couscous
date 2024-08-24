# Recent Activity

## Recently Edited Files

<%*
const dv = app.plugins.plugins["dataview"].api;
const recentlyEditedQuery = `TABLE WITHOUT ID
file.link AS "Note", dateformat(file.mtime, "yyyy-MM-dd") AS "Last Modified"
SORT file.mtime DESC
LIMIT 5`;
const recentlyEditedResult = await dv.queryMarkdown(recentlyEditedQuery);
tR += recentlyEditedResult.value;
%>

## Recently Created Files

<%*
const recentlyCreatedQuery = `TABLE WITHOUT ID
file.link AS "Note", dateformat(file.ctime, "yyyy-MM-dd") AS "Created"
SORT file.ctime DESC
LIMIT 5`;
const recentlyCreatedResult = await dv.queryMarkdown(recentlyCreatedQuery);
tR += recentlyCreatedResult.value;
%>

Last updated: <% tp.date.now("YYYY-MM-DD HH:mm:ss") %>