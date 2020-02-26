List of player skills and abilities IDs

\\This Will Also Serve for AAs\\
\\As well as a baseline for the rest\\

Let's talk about REGEX a bit more here
- FFXIV Network Log Lines

```[09:30:53.841] 15:1004594B:Aho Senpai:07:Attack:4000051C:Striking Dummy:710003:6CA0000:0:0:0:0:0:0:0:0:0:0:0:0:0:0:2862500:2862500:0:0:0:1000:718.0647:267.0143:28.31746:-1.570485:93968:93968:10000:0:0:1000:715.9233:265.7539:28.38361:1.40684:00318599```

Here, we can break that line down. First, we don't really care about the time, so we can ignore that for now

`15:1004594B:Aho Senpai:07:Attack:4000051C:Striking Dummy:710003:6CA0000:0:0:0:0:0:0:0:0:0:0:0:0:0:0:2862500:2862500:0:0:0:1000:718.0647:267.0143:28.31746:-1.570485:93968:93968:10000:0:0:1000:715.9233:265.7539:28.38361:1.40684:00318599`

Then, the whole part that starts with `0:0:0:0` and so on, is mostly data we don't care about (if you do, you probably aren't reading this), so we can strip that part too

`15:1004594B:Aho Senpai:07:Attack:4000051C:Striking Dummy:710003:6CA0000:`

Now that we have the part that interest us, let's see what all of this means

15|1004594B|Aho Senpai|07|Attack|4000051C|Striking Dummy|710003|6CA0000|
---|---|---|---|---|---|---|---|---
Line ID|Caster ID|Caster Name|Ability ID|Ability Name|Target ID|Target Name|*to add exact meaning*|*to add exact meaning*


- "Raw events" Log Lines
