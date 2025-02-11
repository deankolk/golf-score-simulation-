# Golf Score Simulation Project

## Overview

This project takes my personal golf scores and uses them to predict what my future rounds might look like. After running 1000 simulations based on the **Normal Distribution**, the goal is to give me a sense of the range of possible scores I might shoot in upcoming rounds. Whether you’re just curious about your own game or want to get a better idea of what to expect in the future, this simulation is a fun way to see what’s possible.

## Key Features

- **Real Data**: The data comes straight from my own golf scores—no fictional scores here!
- **Statistical Modeling**: The simulation is based on the normal distribution, which was chosen after trying out a few other options.
- **1000 Simulations**: The model runs 1000 simulations to generate a broad range of potential future scores.
- **Data Cleaning**: The data was cleaned and prepped before running the simulations to make sure everything was accurate.
- **Distribution Selection**: After testing several distributions, I used the **Kolmogorov-Smirnov (KS) test** to confirm that the normal distribution was the best fit for my data.

## Methodology

### 1. **Data Cleaning**
The first thing I did was clean up my golf score data. This included:
- Separating multiple columns that were combined together 
- Renaming certain columns that had been named incorrectly when pulling data

### 2. **Testing Distributions**
Before locking in the normal distribution, I wanted to make sure it was the best choice. I tested a few different distributions, including:
- **Normal Distribution**
- **Lognormal Distribution**
- **Exponential Distribution**
- **Gamma Distribution**

To see which one fit the best, I used the **Kolmogorov-Smirnov (KS) test**. The normal distribution came out on top with the highest p-value, meaning it was the best fit for my data.

### 3. **Running Simulations**
Once the normal distribution was chosen, I ran **1000 simulations** to predict future scores. Here’s how it worked:
- First, I calculated the mean and standard deviation of my historical scores.
- Then, I used those values to generate 1000 sets of random scores, simulating what my future rounds could look like based on my past performance.
- This gave me a wide range of possible scores, which helped me understand what to expect in future rounds.

### 4. **Analyzing Results**
After the simulations were complete, I took a deep dive into the results:
- I looked at the **range of possible scores** I might hit in upcoming rounds.
- I calculated the probability of achieving specific scores (for example, the chance of breaking 80 or staying under 90).
- I also analyzed the **variability** of my scores, helping me see how consistent (or not) my performance might be in future rounds.

## Results

The final output is a distribution of simulated future scores based on my past performance. Some key takeaways:
- I now have a good sense of the **likely range** of scores I might shoot in future rounds.
- I can see the **probability** of hitting certain score targets, like breaking 80 or hitting a certain handicap level.
- It gives me a clearer idea of how much **variance** to expect in my game going forward.

## Tools & Technologies

- **Python**: The main language used to build this project.
- **NumPy**: Used for handling numerical operations and generating random numbers.
- **SciPy**: Helped with statistical analysis, particularly the Kolmogorov-Smirnov test.
- **Matplotlib/Seaborn**: Used for visualizing the simulation results.

## Future Improvements

This project is just the beginning, and I’ve got a few ideas on how I can take it further:
- **More detailed stats**: I want to experiment with adding more detailed data like my **handicap**, **putts**, **greens in regulation**, **fairways hit**, and other performance stats to create a more accurate model.
- **More advanced models**: With more data, I could explore more complex modeling techniques, like machine learning, to better capture the nuances of my game.
- **Expanding the dataset**: The more rounds I play and track, the better the model will get. Having more data will make the simulations even more reliable.

