All my notes were showing Jan 30, 2026 under the title.

This is the little date below the title, next to the reading time. I was thinking of it as the "uploaded" date, but Quartz does not really have an uploaded date. It just shows whatever date type you tell it to show.

The problem was in `quartz.config.ts`.

I had:

```ts
defaultDateType: "created",
```

This sounds right, but was not right.

Quartz gets dates from the `CreatedModifiedDate` plugin. Mine checks:

```ts
priority: ["frontmatter", "git", "filesystem"]
```

But the catch is that git is only useful here for `modified`, not really `created`.

So if a note does not have this:

```yaml
---
created: 2024-10-12
---
```

Quartz falls back to the filesystem created date.

And filesystem created date does not mean "when I wrote this note". It can mean "when this file appeared on this computer", or "when Netlify/GitHub/the build machine checked it out", or some other boring file-copying event.

So a bunch of notes ended up looking like they were all created/uploaded on Jan 30, 2026.

The fix was just:

```ts
defaultDateType: "modified",
```

Now the date below the title means "last modified", which is actually a better fit for this whole notes garden thing
basically:


1. `created` without frontmatter = filesystem date nonsense
2. `modified` = git-backed and useful
3. one word config fix



Now it works. 
Yay
