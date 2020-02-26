## :89:Regen: (0x89 = 137)

#### Skill

Example Line  
`[11:03:32.136] 15:1004594B:Aho Senpai:89:Regen:1004594B:Aho Senpai:A0520E:9E0000:1B:898000:0:0:0:0:0:0:0:0:0:0:0:0:90301:90301:10000:0:0:1000:717.3131:265.6258:28.42561:0.55195:90301:90301:10000:0:0:1000:717.3131:265.6258:28.42561:0.55195:0031D30C`

Minimal Regex  
`\[.{14}15:[A-F0-9]{8}:[a-zA-Z-' ]{3,21}:89:`  
(not really used, mostly buff gained/lost is used)

#### Buff

Example Line  
`[11:03:33.156] 1A:1004594B:Aho Senpai gains the effect of Regen from Aho Senpai for 18.00 Seconds.`  
`[11:03:51.122] 1E:1004594B:Aho Senpai loses the effect of Regen from Aho Senpai.`

Practical REGEX  
`\[.{14}1[AE]:[A-F0-9]{8}:(?<target>[a-zA-Z-' ]{3,21}) (?>gains|loses) the effect of Regen from (?<caster>[a-zA-Z-' ]{3,21})(?> for (?<timer>\d{1,2})\.\d{1,2} Seconds)?\.`  
Here, the main issue is that the regex is almost identical to say, Dia  
`\[.{14}1[AE]:[A-F0-9]{8}:(?<target>[a-zA-Z-' ]{3,21}) (?>gains|loses) the effect of Dia from (?<caster>[a-zA-Z-' ]{3,21})(?> for (?<timer>\d{1,2})\.\d{1,2} Seconds)?\.`  
Plus, it's harder to make the regex works on various languages, mainly because there is no SkillID
