# Player Shooting Recommendations

This project generates shooting recommendations for basketball players based on their Points Per Shot (PPS) compared to the league average in different zones on the basketball court.

## Dataset

The dataset used for this analysis contains shot data for players, including x-y coordinates, shot distance, and whether the shot was made or missed.

## Zones Classification

The basketball court is divided into the following zones based on x-y coordinates and shot distance:
- **Restricted Area**: Within 5 feet of the basket.
- **Right Paint (Non-RA)**: 5 to 15 feet from the basket on the right side.
- **Left Paint (Non-RA)**: 5 to 15 feet from the basket on the left side.
- **Right Mid-Range**: 15 to 22 feet from the basket on the right side.
- **Left Mid-Range**: 15 to 22 feet from the basket on the left side.
- **Right Corner 3**: Beyond the three-point line in the right corner.
- **Left Corner 3**: Beyond the three-point line in the left corner.
- **Right Above the Break 3**: Beyond the three-point line on the right side, not in the corner.
- **Left Above the Break 3**: Beyond the three-point line on the left side, not in the corner.

## Methodology

1. **Calculate PPS**:
   - Points per shot (PPS) is calculated as 3 for made three-point shots, 2 for made two-point shots, and 0 for missed shots.

2. **Classify Shots**:
   - Shots are categorized into the defined zones based on x-y coordinates and shot distance.

3. **Calculate Player and League PPS**:
   - The average PPS for each player in each zone is calculated.
   - The league average PPS for each zone is also calculated.

4. **Generate Recommendations**:
   - Recommendations are generated based on the player's PPS compared to the league average PPS.
   - Recommendations include "Shoot More," "Shoot Less," or "Maintain Frequency" based on the player's performance and shot frequency in each zone.

5. **Top Recommendations**:
   - The top 2 to 4 recommendations for each player are selected and formatted into a single string.

6. **Save to CSV**:
   - The final recommendations are saved to a CSV file named `Player_Recommendations.csv`.

## Running the Script

To generate the shooting recommendations, run the provided Python script. The script will create a `Player_Recommendations.csv` file with the following columns:
- **player**: The player's name.
- **recommendations**: The formatted shooting recommendations for the player.

## Example

An example recommendation might look like:
```
James Harden should shoot in the following zones more frequently:
Restricted Area; Mid Range.
```