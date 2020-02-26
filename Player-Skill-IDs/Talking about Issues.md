## Regex-ing Buffs

`\[.{14}1[AE]:[A-F0-9]{8}:(?<target>[a-zA-Z-' ]{3,21}) (?>gains|loses) the effect of Regen from (?<caster>[a-zA-Z-' ]{3,21})(?> for (?<timer>\d{1,2})\.\d{1,2} Seconds)?\.`  
Here, the main issue is that the regex is almost identical to say, Dia  
`\[.{14}1[AE]:[A-F0-9]{8}:(?<target>[a-zA-Z-' ]{3,21}) (?>gains|loses) the effect of Dia from (?<caster>[a-zA-Z-' ]{3,21})(?> for (?<timer>\d{1,2})\.\d{1,2} Seconds)?\.`  
Plus, it's harder to make the regex works on various languages, mainly because there is no SkillID

HOWEVER

the Skill Used log lines does not have the duration.
