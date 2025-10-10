# xG Model for Stevens Women's Soccer

This Python notebook builds an **Expected Goals (xG)** model to evaluate shot quality for the Stevens women’s soccer team. It uses data from professional women’s soccer matches (StatsBomb open data) to predict the probability of a shot becoming a goal based on features like shot location, body part, and whether it was assisted.

## What It Does
- **Loads Data**: Uses ~5,471 shots from women’s pro games (e.g., FA WSL).
- **Cleans Data**: Prepares features like distance to goal, angle, shot type (e.g., header), and context (e.g., assisted, one-on-one).
- **Trains Model**: Builds a logistic regression model to predict xG (0-1 probability).
- **Evaluates**: Achieves ~76% accuracy (ROC AUC 0.7647) in ranking shot quality.
- **Pipeline**: Takes a CSV of Stevens’ game shots (e.g., location, body part), adds an `xG` column, and outputs a new CSV for analysis.
- **Visuals**: Includes a pitch diagram to help estimate shot coordinates from game film.

## Purpose
Helps the team analyze shot quality by assigning xG values (e.g., 0.75 for a penalty, 0.05 for a long shot), identifying good scoring chances, and guiding strategy or training.