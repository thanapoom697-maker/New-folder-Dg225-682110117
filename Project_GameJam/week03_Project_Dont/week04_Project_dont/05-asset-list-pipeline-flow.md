## Asset Pipeline Flow

```mermaid
flowchart TD
    subgraph SOURCES["แหล่ง Asset ที่ใช้"]
        K1[OpenGameArt / itch.io / FreeSound] --> C1[docs/02_Assets/_candidates/]
        K2[Google Fonts / Fontesk] --> C1
    end

    subgraph REPO["Git Repository"]
        C1 --> R1[sprites]
        C1 --> R2[sfx]
        C1 --> R3[music]
        C1 --> R4[fonts]
    end

    subgraph PIPELINE["MonoGame Content Pipeline"]
        R1 --> CP[เลือกและย้ายเข้า Content/]
        R2 --> CP
        R3 --> CP
        R4 --> CP
        CP --> P1[Content.mgcb]
        P1 --> XNB[.xnb files]
    end

    XNB --> GAME[Runtime Game]
```

## แนวทางการจัดการ Asset
- ใช้สไตล์ภาพที่เรียบง่ายแต่สร้างบรรยากาศได้ดี
- เสียงและเอฟเฟกต์ต้องช่วยเพิ่มความรู้สึกกดดันและความไม่ปลอดภัย
- ควรมี asset ที่สามารถ reuse ได้ในหลายฉากเพื่อประหยัดเวลา
