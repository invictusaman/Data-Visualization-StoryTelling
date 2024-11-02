# Kingdom of DataLand

Host/Guide - Roban

King Data - Aman

Waffle Chart - Riddhi

Word Cloud - Amal

Seaborn - Victor

Regression plot - Joy

## Introduction (5 minutes)

**Host (Sage Narrator):** Hello/Bonjour everyone, I’m your charming, beautiful and IBM certified Guide : Sage Narrator, all the way from Kingdom of DataLand. Today we are setting off on a remarkable adventure to explore Data Visualization through Storytelling.

*According to Alberto Cairo,  “Visualization is not about the data; it’s about the story the data can tell.”*

Let us begin our journey.

Kingdom of DataLand is a magical, green, and beautiful realm where data comes alive in vivid forms. It’s a land where insights grow like trees, and knowledge flows like rivers. 

Along our journey, we will meet four incredible data wizards and learn about:

Waffle Charts, Word Clouds, Seaborn and Regression Plots.

Are you ready to Meet the King and four Data Wizards? 

*(Pause - Oh my God Plays)*

## Meet the Characters

**King Data:** Our wise and caring ruler! King Data is always curious, eager to learn about his kingdom’s secrets through the magic of data. He wants to make decisions that truly benefit his people.

**Waffle the Square Wizard:** Hailing from the cozy Square Forests of Wafflewood, Waffle is an expert in waffle charts. These fun charts help us visualize parts of a whole, making it easy to see how things fit together and how they’re distributed.

**Wordy the Cloud Shaper:** The protector of the Whispering Gardens of Wordonia, Wordy has a unique talent for transforming written opinions into beautiful word clouds. These clouds highlight the most common and important words, giving us a quick snapshot of what people are saying.

**Seaborn the Sea Sage:** Living by the Misty Shores of Seaborn Cove, Seaborn uncovers hidden patterns in data with his statistical visuals. His charts help us understand the relationships between different variables, making complex information much easier to digest.

**Reggie the Line Drawer:** Residing in the Predictive Plains of Reggia, Reggie is a master at predicting the future. She draws trend lines through data points to help forecast what might happen next, which is crucial for making smart decisions.

## Objective

**Host:** Over the next hour, we’ll visit each wizard’s realm and see their unique magic in action. King Data will ask important questions, and our wizards will share their insights through their special visualization techniques. By the end of our adventure, you’ll understand how these powerful tools can be used in the real world to guide decisions and inspire action.

So, fasten your seatbelts and prepare for a journey filled with wonder, insights, and a touch of humor. Let the adventure begin!

-----

*(Pause - Drum Plays)*

## Scene 1: The Square Forests of Wafflewood (15 minutes)

**Host:** Our first stop is the Square Forests of Wafflewood, home to Waffle the Square Wizard. 

*(Host will stop moving the cursor, we will transfer control to Waffle.)*

**Waffle:** Welcome, Your Majesty, to my realm of proportions and parts-to-whole relationships!

**King Data:** Greetings, Waffle. I've heard tales of your ability to make complex information clear as day.

**Waffle:** Indeed, Your Majesty. I understand you're having trouble with the kingdom's budget allocation?

**King Data:** Yes, the royal accountants give me sheets full of numbers, but I can never quite grasp the big picture.

**Waffle:** Allow me to assist. Can I see the datasheet, Your Majesty?

**Host:** With a nod of approval, King Data turns to his loyal advisor. 

**King:** Please, present the datasheet to Waffle. Let’s see how she can work her magic!

*(Move to Python code.)*

**Waffle:** Perfect! Watch as I transform this information into a visual feast with my magic word: **"Squares appear, make it clear!"** 

*(Pause - Magic Sound Plays)*

```python
import matplotlib.pyplot as plt
from pywaffle import Waffle

# Data distribution for the kingdom's budget
data = {
    'Defense': 38,
    'Education': 22,
    'Healthcare': 18,
    'Infrastructure': 12,
    'Administration': 10
}

# Create the waffle chart
fig = plt.figure(
    FigureClass=Waffle, 
    rows=5, 
    columns=20,
    values=data, 
    colors = ["#FF0000", "#2196F3", "#4CAF50", "#FFC107", "#9C27B0"],  
    figsize=(22, 12),  
    title={'label': 'Budget Allocation', 'loc': 'center', 'fontsize': 24},
    legend={'loc': 'upper left', 'bbox_to_anchor': (1, 1), 'fontsize': 16}
)

plt.show()
```

**Waffle:** Each square represents 1% of the total budget. The colors represent different categories: red for Defense, blue for Education, green for Healthcare, yellow for Infrastructure, and purple for Administration.

**King Data:** I can see at a glance how our money is distributed just by counting colored squares!. The red squares for Defense do take up a large portion.

**King Data:** But how can our ministers use this in their day-to-day work?

**Waffle:** Great question, Your Majesty! Let me show you how this can be done using Excel.

*(Excel Explanation)*

**King Data:** Remarkable! This will make budget discussions so much easier. Thank you, Waffle!

**Host:** And so, King Data learned the power of waffle charts in visualizing parts of a whole. As we leave the Square Forests, we can see the king already planning how to use this magic in his next royal budget meeting.

*(At this point, Waffle will start asking questions from the slides. Once done, revoke the remote control from Zoom.)*

*(Pause on Who wants to be a Data Analyst Slide - Music Plays)*

----

*(Pause - Drum Music Plays)*

## Scene 2: The Whispering Gardens of Wordonia (15 minutes)

**Host:** Our next stop is the Whispering Gardens of Wordonia, where words float in the air like leaves on the wind. Here we meet Wordy the Cloud Shaper.

*(At this time, we will transfer control to Wordy.)*

**Wordy:** Welcome, Your Majesty, to my garden of lexical wonders!

**King Data:** Wordy, I'm amazed! The words... they're floating and changing size!

**Wordy:** Indeed, Your Majesty. I hear you've been having trouble understanding your subjects' opinions about the new royal park. Perhaps I can help?

**King Data:** Oh, yes! We've received hundreds of comments, but it's overwhelming to read them all.

**Wordy:** Fear not! I can shape these words into a meaningful cloud. But first, I need the comments data.

**Host:** With a nod of approval, King Data grants permission and his minister shares the data.

*(Move to Python Code.)*

**Wordy:** Excellent! Let me spell my Magic words : **"Words so light, float in sight!"**

*(Pause - Magic Sound Plays)*

```python
from wordcloud import WordCloud, STOPWORDS
import matplotlib.pyplot as plt

# Sample text based on the park comments
text = """
Beautiful beautiful beautiful relaxing relaxing green peaceful
needs more benches lovely tranquil scenic picturesque family-friendly
clean well-maintained needs more shade calm serene beautiful relaxing
"""
custom_stopwords = set(STOPWORDS)
custom_stopwords.update(["needs"])  # Add specific words to ignore

# Create and generate a word cloud image, ignoring stopwords

wordcloud = WordCloud(width=800, height=400, background_color='white', stopwords=custom_stopwords).generate(text)

# Display the generated image
plt.figure(figsize=(10, 5))
plt.imshow(wordcloud, interpolation='bilinear')
plt.axis('off')
plt.title('Citizen Feedback on the Royal Park')
plt.show()
```

**Wordy:** In this cloud, the size of each word represents how frequently it was mentioned. See how "beautiful" and "relaxing" are quite large?

**King Data:** Fascinating! And I can see "more benches" is smaller but still noticeable.

**Wordy:** Exactly! Now, Your Majesty, based on this word cloud, what do you think should be your next action regarding the park?

**King Data:** Well, it seems adding more benches would be a good start. It would address the main criticism while maintaining the beautiful and relaxing atmosphere people love.

**Wordy:** A wise decision, Your Majesty! 

**King Data:** This is delightful! But how can our gardeners use this practically?

**Wordy:** Let's see how we can create this in IBM Cognos.

*(IBM Cognos Explanation)*

**King Data:** Great. Thank you Wordy.

**Host:** As we leave the Whispering Gardens, King Data is already drafting a decree to add more benches to the royal park, thanks to the insights gained from Wordy's magical word cloud.

*(At this point, Wordy will start asking questions from the slides. Once done, revoke the remote control from Zoom.)*

*(Pause on Who wants to be a Data Analyst Slide - Music Plays)*

---

*(Pause - Drum Music Plays)*

## Scene 3: The Misty Shores of Seaborn Cove (15 minutes)

**Host:** We now arrive at the Misty Shores of Seaborn Cove, where data flows like water and patterns emerge from the fog. Here we meet Seaborn the Sea Sage.

*(At this time, we will transfer screen control to Sea Sage.)*

**SeaSage:** Greetings, Your Majesty! Welcome to the realm of hidden patterns and relationships.

**King Data:** Seasage, I've heard you can reveal insights that are invisible to the naked eye.

**SeaSage:** Indeed, Your Highness. I understand you're curious about the health of your subjects?

**King Data:** Yes, particularly the relationship between their height and weight. Our royal physicians have collected data, but we're unsure what it means.

*(Move to Python Code.)*

**SeaSage:** Allow me to illuminate this for you by waving my trident and spelling the magic cast: **"Waves of data, show your form!"**

*(Pause - Magic Sound Plays)*

```python
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd

# Generate some sample data
np.random.seed(0)
n = 100
heights = np.random.uniform(150, 200, n)
weights = 0.5 * heights + np.random.normal(0, 10, n)

# Create a DataFrame
data = pd.DataFrame({'Height (cm)': heights, 'Weight (kg)': weights})

# Create the scatter plot with regression line
plt.figure(figsize=(10, 6))
sns.regplot(x='Height (cm)', y='Weight (kg)', data=data, scatter_kws={'alpha':0.5})
plt.title('Relationship between Height and Weight in the Kingdom')
plt.show()
```

**SeaSage:** Each point of light represents one of your subjects, with their height on one axis and weight on the other.

**King Data:** Incredible! I can see a pattern forming... it seems that generally, taller people tend to weigh more.

**SeaSage:** Well observed, Your Majesty! This line represents the general trend of the relationship between height and weight.

**King Data:** I see some points far from the line. What do they mean?

**SeaSage:** An astute observation, Your Highness! Those points could represent individuals who are particularly muscular, or perhaps those struggling with obesity. Now, Your Majesty, based on this visualization, what health initiative might you consider for the kingdom?

**King Data:** Well, perhaps we should focus on nutrition and exercise programs, particularly for those falling far above the trend line.

**SeaSage:** A wise decision, Majesty! You've just used statistical visualization to inform public health policy.

**Host:** As we depart from Seaborn Cove, King Data is already planning a new royal fitness program, inspired by the insights from Seaborn's magical scatter plot.

*(At this point, SeaSage will start asking questions from the slides. Once done, revoke the remote control from Zoom.)*

*(Pause on Who wants to be a Data Analyst Slide - Music Plays)*

---

*(Pause - Drum Music Plays)*

## Scene 4: The Predictive Plains of Reggia (15 minutes)

**Host:** Our final destination is the Predictive Plains of Reggia, where the future shimmers on the horizon. Here we meet Reggie the Line Drawer.

*(At this time, we will transfer screen control to Reggie.)*

**Reggie:** Welcome, Your Majesty, to the land where past trends foretell future outcomes!

**King Data:** Reggie, I'm told you can peer into the future. Is this true?

**Reggie:** In a manner of speaking, Your Majesty. I understand you're concerned about future crop yields?

**King Data:** Indeed! Our farmers are worried about how changing rainfall might affect their harvests. 

**Host:** King informs ministers to share the information.

*(Move to Python Code.)*

**Reggie:** I can help you visualize this relationship. Now, observe as I draw the lines of fate by spelling my magic spell: **"Points align, future divine!"**

*(Pause - Magic Sound Plays)*

```python
import numpy as np
import matplotlib.pyplot as plt
from scipy.stats import linregress

# Generate some sample data
np.random.seed(0)
rainfall = np.random.uniform(500, 1000, 20)
crop_yield = 0.1 * rainfall + np.random.normal(0, 5, 20)

# Create the scatter plot
plt.figure(figsize=(10, 6))
plt.scatter(rainfall, crop_yield, alpha=0.5)

# Calculate and plot the regression line
slope, intercept, r_value, p_value, std_err = linregress(rainfall, crop_yield)
line = slope * rainfall + intercept
plt.plot(rainfall, line, color='r', label='Trend Line')

# Extend the line for future prediction
future_rainfall = np.linspace(400, 1100, 100)
future_yield = slope * future_rainfall + intercept
plt.plot(future_rainfall, future_yield, color='r', linestyle='--', label='Future Prediction')

plt.xlabel('Annual Rainfall (mm)')
plt.ylabel('Crop Yield (bushels per acre)')
plt.title('Crop Yield vs Rainfall in the Kingdom')
plt.legend()
plt.show()
```

**Reggie:** Your Majesty, the chart shows a clear relationship between annual rainfall and crop yield. Each point represents a year, with rainfall on the horizontal axis and crop yield on the vertical axis.

**King Data:** I see. And what about that red line?

**Reggie**: The solid red line is the trend line, Your Highness. It shows the overall pattern in the data. The dashed part extends this trend to predict future outcomes.

**King Data:** Interesting! So what's the main conclusion we can draw from this?

**Reggie:** Well, Sire, the trend is unmistakably upward. As rainfall increases, crop yields tend to increase as well. This holds true across the entire range of data we have.

**King Data:** So you're saying more rain always means better crops?

**Reggie:** Based on this data, yes, Your Highness. At least within the range we've observed. The relationship appears consistently positive. Even our future predictions, shown by the dashed line, continue this upward trend.

**King Data:** That's not what I expected. I thought there'd be a sweet spot, with yields dropping if we got too much rain.

**Reggie:** It's a surprising result, Sire.

**King Data:** Remarkable! But how can our farmers use this knowledge in their daily work?

**Reggie:** Excellent question! Let's see how we can implement this in Google Looker Studio.

*(Looker Studio Explanation)*

**King Data:** Thank you Reggie for detailed insights.

**Host:** As we leave the Predictive Plains, King Data is already drafting plans for a new royal water management system, inspired by Reggie's prophetic trend lines.

*(At this point, Reggie will start asking questions from the slides. Once done, revoke the remote control from Zoom.)*

*(Pause on Who wants to be a Data Analyst Slide - Music Plays)*

---

*(Pause - Drum Music Plays)*

## Conclusion (5 minutes)

**Host:** And so, our journey through the Magical Data Visualization Kingdom comes to an end. We've seen how Waffle's square forests, Wordy's whispering gardens, Seaborn's misty cove, and Reggie's predictive plains have all helped King Data gain new insights and make informed decisions.

**King Data:** Thank you, magical wizards! You've shown me that the true power of data lies not in the numbers themselves, but in how we visualize and interpret them. From now on, the Kingdom of DataLand shall rule with the wisdom of data visualization!

**Host:** And thus, dear audience, we conclude our tale. May you too find the magic in your data, transforming numbers into insights and actions. Farewell from the Magical Data Visualization Kingdom!

Thank you all for listening! Any Questions?

-----

*Story concept by Aman Bhattarai.*
