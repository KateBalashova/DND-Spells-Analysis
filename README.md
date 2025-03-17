# Dungeons and Dragons Spells Dataset Analysis

## Description
The dataset that we chose to work on is called **Dungeons and Dragons Spells (2024)** and contains information about the 315 spells included in the 2024 edition of Dungeons and Dragons Free Rules. Each spell is described using **27 parameters**, such as the spell’s name, level, school, materials required for casting, availability to different classes, range, duration, and text description.

## Reason
We chose the **Dungeons and Dragons spells dataset** because it combines creativity with structured attributes, making it ideal for data visualization. The dataset's rich details—such as spell levels, schools of magic, casting times, and components—provide diverse variables to analyze and present. Additionally, the classification of spells by character classes adds an intriguing layer of complexity, appealing to both our interest in fantasy and our aim to demonstrate effective visualization techniques for categorical and numerical data.

## Questions
1. **How do common words used in spell names and descriptions vary in accordance with the classes that can use the spell?**
2. **What influence do the level of the spell and the presence of verbal, somatic, and material components have on its range?**

## Plan

### Preprocessing
1. Use the provided cleaning script by the author.
2. Stem or lemmatize words to unify similar forms (e.g., "cast" and "casting") if needed.

### Question 1
- Process the text in the `description` and `name` columns.
- Try out different text representations (e.g., Bag-of-Words, TF-IDF) to identify which method yields more meaningful insights.
- Compare the top words for each class and investigate overlaps or distinctive keywords (e.g., are words like "healing" more frequent for clerics, while "illusion" is common for wizards?).
- **Final Output**: A word cloud (or series of word clouds) for each of the 8 spellcasting classes.

### Question 2
- Research methods to work with the `range` column (an ordered categorical variable).
- Explore which visual representation provides the most information about the determinants of range:
  - Range versus `level` and the **number of components** (scatterplot).
  - Range versus `level` and **component combinations** (heatmap).
- Use a combination of spell level and components to predict or identify trends in range:
  - For example:
    - **High level + all three components** = longer ranges?
    - **Low level + only verbal_component** = shorter ranges?
- Analyze how the inclusion of multiple components (e.g., `verbal_component` + `material_component`) influences the range.
