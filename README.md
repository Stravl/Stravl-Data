# Stravl-Data

Stravl-Data is the world's largest, open-sourced data set of travel preferences. Through a user-facing website, Stravl gathered 80,301 travelers' vacation preferences. Users were asked to fill out a brief form on their ideal vacation preferences (such as expected experiences, scenery, and activity level) and logistical constraints (such as budget, traveler ages, and season). Thereafter, they were asked to "swipe" or "rate" ten destinations. Users have the option to respond with "Yes", "No", or "Maybe" in a Tinder-like rating framework. In total, over 1,000,000 user swipes were recorded. Lastly, users are shown 5 to 10 recommendations, which were selected using different ML-models. Those recommendations are recorded and users' feedback on them (through clicking a "smiley" or "frowny" face next to them) is stored. Personally-identifying information such as IP data, user names, or other metadata has been removed prior to the release of this dataset.

Stravl's extensive travel preference data is the largest custom data set of its kind. You are free to use the data for any academic or commercial purposes. We're happy to help with questions, just reach out to info@stravl.com. Below find a brief description of all columns in our data set.

## Form Responses:

### FORM_A: 
What age ranges are present in your travel group? [multiple selections possible]

- 0: 0-19
- 1: 20-39
- 2: 40-59
- 3: 60+

### FORM_B: 
What is your trip budget (per person, per night)?

- 0: $0-$49
- 1: $50-$99
- 2: $100-$249
- 3: $300+

### FORM_C: 
What season are you planning to travel?

- 0: Winter
- 1: Spring
- 2: Summer
- 3: Fall

### FORM_F: 
What are you looking to experience? Multiple selections encouraged.

- 0: Beach
- 1: Adventure
- 2: Nature
- 3: Culture
- 4: Nightlife
- 5: History
- 6: Shopping
- 7: Cuisine

### FORM_G: 
What scenery are you seeking? Multiple selections encouraged.

- 0: Urban
- 1: Rural
- 2: Sea
- 3: Mountain
- 4: Lake
- 5: Desert
- 6: Plains
- 7: Jungle

### FORM_H: 
Activity Level

- 0: Chill & Relaxed
- 1: Balanced
- 2: Active

### FORM_I: 
Safety Conscious

- 0: Very Safety Conscious
- 1: Balanced
- 2: Ready for Anything

### FORM_J: 
Destination Popularity

- 0: Off the Beaten Path
- 1: Classic Spot
- 2: Mainstream & Trendy

### FORM_R: 
Where do you want to go?

- 0: Anywhere
- 1: Specific Regions

### FORM_RR: 
Which specific regions? [If ‘Specific Regions’ is selected in FORM_R] [multiple selections allowed]

- e: Europe
- n: N. America
- c: Caribbean
- a: Asia
- s: S. America
- m: Mid. East
- f: Africa
- o: Oceania

## Swipe Responses:
Each of "yes_swipes", "no_swipes", and "maybe_swipes" includes a list of indices representing destinations a user swiped 'yes', 'no', or 'maybe' on. The indices can be transformed to its corresponding destination names through the "destination_ids" table.

##  Model, Recommendations, and Ratings:
Users were then recommended a set of 5 destinations (or 10 if a user wanted more). Different algorithms were used to recommend those destinations; the variables "model", "retrieval", and "dynaMatch" indicate which algorithms were used. Their implementations are not released, yet their selections are still shared for research purposes.

Each of the recommendation columns includes the names of recommended destinations in order of recommendation; if a column includes '-1' recommendations were not yet tracked at the time this user completed the form. Each rating column includes ant user ratings that were provided. If all ten columns are set to -1, ratings were not tracked at the time this user completed the form. If not, a rating of '-1' indicates a user's disapproval with the rating, and a rating of '1' indicates their approval of it. If the entry is empty, the user has not rated the corresponding destination.
