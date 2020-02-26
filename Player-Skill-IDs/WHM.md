# WHM IDs

Hex Line | Hex ID | Name | Dec ID | Dec Line
:---:|:---:|:---:|:---:|:---:
15|78|Cure  
15|87|Cure II
15|4093|Afflatus Solace
15|89|Regen
15|77|Stone
15|7F|Stone II
15|DF0|Stone III
15|D107|Stone IV
15|4095|Glare
15|79|Aero  
15|84|Aero II  
15|4094|Dia
15|8C|Benediction
15|DF2|Tetragrammaton  
15|1D08|Divine Benison  
15|4098|Temperance  
15|86|Fluid Aura  
15|1D06|Thin Air
15|88|Presence Of Mind 
15|7D|Raise 
1[56]|7C|Medica  
1[56]|83|Cure III  
1[56]|85|Medica II  
1[56]|DF3|Assize  
1[56]|4096|Afflatus Rapture
1[56]|4097|Afflatus Misery
1[56]?|1D09|Plenary Indulgence
16|DF1|Asylum  



### :89:Regen: (0x89 = 137)

##### Skill

Example Line  
`[11:03:32.136] 15:1004594B:Aho Senpai:89:Regen:1004594B:Aho Senpai:A0520E:9E0000:1B:898000:0:0:0:0:0:0:0:0:0:0:0:0:90301:90301:10000:0:0:1000:717.3131:265.6258:28.42561:0.55195:90301:90301:10000:0:0:1000:717.3131:265.6258:28.42561:0.55195:0031D30C`

Minimal Regex  
`\[.{14}15:[A-F0-9]{8}:[a-zA-Z-' ]{3,21}:89:`  
(not really used, mostly buff gained/lost is used)

##### Buff

Example Line  
`[11:03:33.156] 1A:1004594B:Aho Senpai gains the effect of Regen from Aho Senpai for 18.00 Seconds.`  
`[11:03:51.122] 1E:1004594B:Aho Senpai loses the effect of Regen from Aho Senpai.`

"Practical" REGEX  
`\[.{14}1[AE]:[A-F0-9]{8}:(?<target>[a-zA-Z-' ]{3,21}) (?>gains|loses) the effect of Regen from (?<caster>[a-zA-Z-' ]{3,21})(?> for (?<timer>\d{1,2})\.\d{1,2} Seconds)?\.`  

### Tetragrammaton

##### Skill

Example Line  
`[11:03:34.278] 15:1004594B:Aho Senpai:DF2:Tetragrammaton:1004594B:Aho Senpai:4:70250000:0:0:0:0:0:0:0:0:0:0:0:0:0:0:90301:90301:9500:0:0:1000:717.3131:265.6258:28.42561:0.55195:90301:90301:9500:0:0:1000:717.3131:265.6258:28.42561:0.55195:0031D30F`

### Dia

##### Skill

Example Line  
`[11:03:35.394] 15:1004594B:Aho Senpai:4094:Dia:4000051C:Striking Dummy:750003:1AB00000:A0FB0E:74F0000:1B:40948000:0:0:0:0:0:0:0:0:0:0:2862410:2862500:0:0:0:1000:718.0647:267.0143:28.31746:-1.570485:90301:90301:9798:0:0:1000:717.3131:265.6258:28.42561:0.4961289:0031D311`

