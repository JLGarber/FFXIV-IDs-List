

:89:Regen:  
:DF2:Tetragrammaton:  
:4094:Dia:  
:1D08:Divine Benison:  
:4095:Glare:  
:87:Cure II:  
:78:Cure:  
:4098:Temperance:  
:1D06:Thin Air:  
:8C:Benediction:  
:88:Presence Of Mind:  
:86:Fluid Aura:  
:4093:Afflatus Solace:  


:DF1:Asylum: (16:)  


:DF3:Assize: (1[56]:)  
:85:Medica II: (1[56]:)  
:83:Cure III: (1[56]:)  
:7C:Medica: (1[56]:)  
:4096:Afflatus Rapture: (1[56]:)  
:4097:Afflatus Misery: (1[56]:)

? :1D09:Plenary Indulgence: (1[56]:)?  


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

"Practical" REGEX  
`\[.{14}1[AE]:[A-F0-9]{8}:(?<target>[a-zA-Z-' ]{3,21}) (?>gains|loses) the effect of Regen from (?<caster>[a-zA-Z-' ]{3,21})(?> for (?<timer>\d{1,2})\.\d{1,2} Seconds)?\.`  
