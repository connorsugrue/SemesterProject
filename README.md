<!-- #region -->
# SemesterProject

**The 2 main files we have worked with for this project are "Correlation_Plots_And_Decision_Boundaries.ipynb" and the "Correlation_Matrix.ipynb" The rest of the files are for our own reference.

Our project revolved around statistics within the NBA. We looked at 4 main factors Record, Points Scored, Offensive and Defensive efficiency and historic data which helped us predic the winner of the NBA finals.

# Part 1
We first took in a plethora of data sets listed below and extracted all of the data from it.

team_stats_all_time

team_playoff_stats_all_time

player_stats_extra

team_stats_2022_2023

player_stats

We then looked at the correlation of many different statistics with the win

# Part 2
The code defines three different mathematical functions (exp, quad, and linear) for fitting curves to data points. These functions take input parameters (x, a, b, c) and return calculated values based on those parameters.

Specifically:

exp calculates a raised to the power of (x * b). quad calculates a quadratic equation of the form ax^2 + bx + c using the input parameters a, b, c, and x. linear calculates a linear equation of the form a*x + b using the input parameters a, b, and x. The code then uses the curve_fit function, presumably from the scipy.optimize module, to find the best-fit parameters (best_fit_parameters) for the exp function based on the data in the team_stats_all_time DataFrame for the columns 'PTS' and 'W'. The curve_fit function is commonly used for fitting curves to data points using non-linear regression.

Finally, the code uses the plt module from the matplotlib library, to create a scatter plot of the data points ('PTS' vs 'W') using plt.scatter(), and overlays a plot of the best-fit exponential curve using plt.plot() with the calculated exp_fit values.

We did this for each of the different stats we identified creating correleation plots

# Part 3

We then went through all of our data sets and sepreated the championship teams from the data set and placed them in their own data sets so we had a comparison of what the group of championship stats looked like compared to non championship teams

# Part 4

We went through the key statistics we indetified and plotted wins vs that statistic. We plotted both the championship teams(in blue) and the non championship teams (in orange) to help us figure out where the decision boundry should be. 

We then took these same plots and plotted that decison boundry as a blue line which was the averaged out stats. 

On a deeper level

This code uses matplotlib to create scatter plots of data from two different data sources, championshipdf and team_stats_all_time, representing wins and field goal percentage (FG%) for a particular sports team or teams.

The code first uses plt.scatter() function to create scatter plots, where championshipdf['W'] and championshipdf['FG%'] are used as the x and y values respectively for the first scatter plot, and team_stats_all_time['W'] and team_stats_all_time['FG%'] are used as the x and y values respectively for the second scatter plot. This will create two separate scatter plots with wins on the x-axis and FG% on the y-axis.

Next, plt.title(), plt.xlabel(), and plt.ylabel() functions are used to set the title, x-axis label, and y-axis label for the plot, respectively.

Finally, plt.axvline(55) adds a vertical line at x-axis value 55 on the plot. This could be used as a reference line to indicate a specific value of wins, such as a threshold or benchmark. The purpose of this line would depend on the context of the data and the analysis being performed.


# Part 5 

We then finally took those decison boundries we created to go game by game in the 2023 realsed NBA playoff bracket. We ploted each matchup with the each of the stats chosen against the decison boundry and the team on the right had the advantage and the team on the left had the disadvantage. When both teams were on the left we dicided to look at the home court adavantage to decide the winner. After going through each match up we have determined that the Boston Celtics will win the 2023 NBA championship.  

<!-- #endregion -->
