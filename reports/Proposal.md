# Dungeons and Dragons Spells Dataset Analysis

## Description
The dataset that we chose to work on is called **Dungeons and Dragons Spells (2024)** and contains information about the 315 spells included in the 2024 edition of **Dungeons and Dragons Free Rules**. Each spell is described using 27 parameters, such as the spell’s name, level, school, materials required for casting, availability to different classes, range, duration, and text description.

## Reason
We chose the **Dungeons and Dragons spells dataset** because it combines creativity with structured attributes, making it ideal for data visualization. The dataset's rich details—such as spell levels, schools of magic, casting times, and components—provide diverse variables to analyze and present. Additionally, the classification of spells by character classes adds an intriguing layer of complexity, appealing to both our interest in fantasy and our aim to demonstrate effective visualization techniques for categorical and numerical data.

## Questions
1. **How do common words used in spell names and descriptions vary in accordance with the classes that can use the spell?**
2. **What influence do the level of the spell and the presence of verbal, somatic, and material components have on its range?**

## Plan

### Preprocessing
1. Use the provided cleaning script by the author.
2. Stem or lemmatize words to unify similar forms (e.g., "cast" and "casting") if needed.
3. Remove punctuation, stop words, and perform case normalization.
4. Map categorical distances to numerical values or ordinal encoding (e.g., Touch < 30 ft < 60 ft < 120 ft < Unlimited).
5. Check for and handle missing values and outliers in relevant columns.

---

## Question 1: Language Variations by Class

### Objective
Determine how the language of spells differs by the class that can cast them.

### Approach
- Preprocess the text in the **description** and **name** columns.
- Try out different text representations (e.g., **TF-IDF**) to identify which method yields more meaningful insights.
- Compare relevance for each representation.
- Compare the top words for each class and investigate overlaps or distinctive keywords (e.g., are words like "healing" more frequent for **clerics**, while "illusion" is common for **wizards**?).

### Visualizations
- **Interactive Wordcloud** allowing the user to view the most distinctive words for selected classes.

### Analysis
- Identify unique terms for each class (e.g., “healing” in Cleric spells vs. “illusion” in Wizard spells).
- Discuss patterns and possible thematic connections to the class’s role.

---

## Question 2: Influence of Spell Level and Components on Range

### Objective
Understand how a spell’s level and components (verbal, somatic, material) relate to its range.

### Approach
- Preprocess the **range** column.
- Create new variables:
  - **Component count**: total number of components required (0–3).
  - **Component combinations**: (e.g., “V”, “V+S”, “V+S+M”).
  
### Visualizations
- **Scatter plot**: Range vs. Spell Level. Use color or size to indicate the number of components.
- **Heatmap**: Rows = Spell Level, Columns = Component Combination. Values = Average Range.

### Analysis
- Identify trends such as:
  - Do higher-level spells tend to have longer ranges?
  - Does the presence of more components correlate with greater range?
  - Are spells with only verbal components typically short-ranged?

---

## Conclusion
This analysis aims to provide a deeper understanding of the Dungeons and Dragons spell mechanics, focusing on the relationship between spell components, classes, and their range and level. The combination of textual and numerical data offers a rich set of insights that can help inform the design of both game mechanics and character strategies.
