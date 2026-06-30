```mermaid
mindmap
root((Pac-Man))
   Theme
     เขาวงกต
     อาเขตยุค 80
   Mechanics
     เดินในเขาวงกต
     กิน Pellet
    Power Pellet
 Content
    ผีศัตรู 4 ตัว
    ผลไม้โบนัส
    วิ่งไล่กินผี
 Audience
    ผู้เล่น Casual
 High Score / Online Leaderboard
    รับของรางวัล
    โชว์ชื่อเรา
```

## we adjust Hight Score/Online Leaderboard

```mermaid
quadrantChart
 title Pac-Man — Feature Prioritization
 x-axis Low Effort --> High Effort
 y-axis Low Impact --> High Impact
 quadrant-1 Quick Wins
 quadrant-2 Major
 quadrant-3 Nice to Have
 quadrant-4 Reconsider
 Maze Movement: [0.3, 0.95]
 Ghost AI: [0.7, 0.9]
 Online Leaderboard: [0.7, 0.3]
 bonus item : [0.5,0.5]
 them:[0.3,0.3]
 skin:[0.2,0.3]
 sfx:[0.7,0.7]
```

## we adjust 'bonus item, them, skin, sfx'

```mermaid
gantt
 title Pac-Man — Production Timeline (6 สัปดาห์)
 dateFormat YYYY-MM-DD
 section Pre-Production
 Concept & GDD :done, c1, 2026-07-06, 5d
 section Production
 Maze Movement :active, p1, after c1, 5d
 Ghost AI : p2, after p1, 7d
 Pellet & Score : p3, after p2, 7d
 SFX : p3, after p2, 7d
 section Post
 QA & Bug Fix : q1, after p3, 5d
 Release Build :milestone, m1, after q1, 0d
```

## we adjust SFX

