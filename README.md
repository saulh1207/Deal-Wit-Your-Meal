# About
The following is a group project where we aimed to create a bot that would ask a user questions of meal preferences and restrictions, then output recipe suggestions in return.

# Source
Our source data is a Food.com dataset holding ~230,000 recipes along with descriptional tags, nutritional values, ingredients, and steps to follow for each.

# Architecture & Methods
- We utilized Watson Assistant to create the chat bot, the trained JSON version of which you will see included.
- Our backend was housed within IBM Cloud Functions, and our dataset within IBM Cloud Storage.
- A webhook would provide the entered responses to our Cloud Functions code, where we used content-based filtering to select a handful of recipes.
- The last question asked to the user is a breif description of what they are looking to make, which we then used to rank the last few recipes with cosine similarity, returning 3 recipes that closely match what the user was looking for.

# Collaborators
This was worked on by Saul Hernandez (myself), Andrew Masur, and Jack Valian
