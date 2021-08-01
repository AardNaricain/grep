# grep

Creates a grep command for aardwolf, similar to the unix grep.

Say you have a bag full of equipment and you want to look for axes. You could `examine bag`
```
     (K) (Magic) (Glow) (Hum) the Amulet of Aardwolf (1)
     (K) (Magic) (Glow) (Hum) Wings of Aardwolf (1)
     (K) (Magic) (Glow) (Hum) Aardwolf Helm of True Sight (2)
     (K) (Magic) (Glow) (Hum) Aardwolf Gloves of Dexterity (5)
( 2) (K) (Magic) (Glow) (Hum) Axe of Aardwolf (80)
     (K) (Magic) (Glow) (Hum) Aardwolf Breastplate of Magic Resistance (1)
     (K) (Magic) (Glow) (Hum) the Shield of Aardwolf (1)
     (K) (Magic) (Glow) (Hum) Aardwolf Ring of Regeneration (32)
     (K) (Magic) (Glow) (Hum) Aardwolf Bracers of Iron Grip (60)
     (K) (Magic) (Glow) (Hum) Axe of Aardwolf (151)
     (K) (Magic) (Glow) (Hum) Aardwolf Ring of Invisibility (5)
     (K) (Magic) (Glow) (Hum) Aardwolf Aura of Sanctuary (1)
     (K) (Magic) (Glow) (Hum) Dagger of Aardwolf (140)
     (K) (Magic) (Glow) (Hum) Aardwolf Breastplate of Magic Resistance (21)
     (K) (Magic) (Glow) (Hum) Aardwolf Helm of True Sight (7)
     (K) (Magic) (Glow) (Hum) Axe of Aardwolf (20)
     (K) (Magic) (Glow) (Hum) the Shield of Aardwolf (100)
     (K) (Magic) (Glow) (Hum) Dagger of Aardwolf (201)
```

Ugh, too much stuff. Manuually reading is annoying. Let's try that again with grep
`examine bag | grep axe`
```
( 2) (K) (Magic) (Glow) (Hum) Axe of Aardwolf (80)
     (K) (Magic) (Glow) (Hum) Axe of Aardwolf (151)
     (K) (Magic) (Glow) (Hum) Axe of Aardwolf (20)
```

Much better!

It also works with regular expressions:
`examine bag | grep \(\d{1}\)`
```
     (K) (Magic) (Glow) (Hum) the Amulet of Aardwolf (1)
     (K) (Magic) (Glow) (Hum) Wings of Aardwolf (1)
     (K) (Magic) (Glow) (Hum) Aardwolf Helm of True Sight (2)
     (K) (Magic) (Glow) (Hum) Aardwolf Gloves of Dexterity (5)
     (K) (Magic) (Glow) (Hum) Aardwolf Breastplate of Magic Resistance (1)
     (K) (Magic) (Glow) (Hum) Aardwolf Bracers of Iron Grip (1)
     (K) (Magic) (Glow) (Hum) the Shield of Aardwolf (1)
     (K) (Magic) (Glow) (Hum) Aardwolf Ring of Invisibility (5)
     (K) (Magic) (Glow) (Hum) Aardwolf Aura of Sanctuary (1)
     (K) (Magic) (Glow) (Hum) Aardwolf Helm of True Sight (7)
```


