---
type: gdd-mechanics
version: 0.1
date: [14/07/26]
---
# Mechanic Design — [ชื่อ Mechanic]

## State Diagram

```mermaid
stateDiagram-v2
    [*] --> Idle
    Idle --> move : click item or place
    move --> Int : colect item
Int --> move
move --> Idle
  Idle --> Cutsceen_fight: follow dialogue face an enemy
 Cutsceen_fight --> lose: dead
  Cutsceen_fight --> win: survie
win --> Idle
 lose --> End




   
 

  
  
   
```

## Rules

| State    | เข้าเงื่อนไข                            | ออกเงื่อนไข                             | Note               |
| -------- | --------------------------------------------------- | -------------------------------------------------- | ------------------ |
| Idle     | เมื่อตัวละครอยู่นิ่ง            | เมื่อมีการเคลื่อนไหว           | Animation loop     |
| Move     | กดไปตามพื้นที่                        | เมื่อตัวละครหยุดนิ่ง           | Speed              |
| Int      | กดไปที่ไอเทม                            | เมื่อไม่มีการคลิกที่ไอเทม | Interact with item |
| Cutsceen | เมื่อenemyเข้าในระยะที่กำหนด | เมื่อไม่อยู่ในระยะ               | Quick time event   |
| lose     | เมื่อแพ้ในcutsceen                        | เมื่อชนะcutsceen                           | lose               |
| End      | เมื่อชนะcutsceen                            | เมื่อแพ้ในcutsceen                       | Renew game         |
