## 📦 Dungeons and Dragons Spells (2024) Dataset

This dataset contains detailed information on **314 spells** from the **2024 edition of the Dungeons & Dragons Free Rules**. Each spell is richly described with **27 features**, ranging from school of magic, casting components, range, duration, and class availability.

---

### 🧙‍♂️ Provenance

- **Source**: [TidyTuesday - Week 13, 2024](https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-03-26/readme.md)
- **Original Data Author**: [Matthew Whited](https://github.com/mwthomas)  
- **Compiled for**: TidyTuesday, a weekly data project from the R for Data Science community
- **Raw Data License**: Shared for educational and visualization purposes
- **Dataset URL**: [DND Spells CSV](https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-03-26/dnd_spells.csv)

---

### 📘 Codebook (Feature Descriptions)

| Column                        | Description |
|------------------------------|-------------|
| `name`                       | Name of the spell |
| `level`                      | Spell level (0 = Cantrip, 1–9 = Leveled spells) |
| `school`                     | School of magic (e.g., evocation, illusion) |
| `bard`, `cleric`, ...        | Boolean flags indicating which classes can cast the spell |
| `casting_time`               | Standard casting time (e.g., 1 action, 1 minute) |
| `action`, `bonus_action`, `reaction` | Indicates casting timing type |
| `ritual`                     | Whether the spell can be cast as a ritual |
| `casting_time_long`          | Extended description of casting time (if applicable) |
| `trigger`                    | Specific trigger for casting (only used for a few spells) |
| `range`                      | Spell range (e.g., 60 feet, Self) |
| `range_type`                 | Categorized range type (feet, self, touch, etc.) |
| `verbal_component`           | Whether the spell requires verbal components |
| `somatic_component`          | Whether the spell requires somatic components |
| `material_component`         | Whether the spell requires material components |
| `material_component_details`| Details of material components (if applicable) |
| `duration`                   | How long the spell lasts |
| `concentration`              | Whether the spell requires concentration |
| `description`                | Full description of the spell's effect |

---

### 📊 Summary

- **Total Spells**: 314
- **Total Features**: 27
- **Class Support**: Includes support info for 8 main classes (e.g., bard, wizard)
- **Component Details**: Specifies whether verbal, somatic, and material components are needed
- **Rich Text**: Each spell has a full description for NLP analysis

