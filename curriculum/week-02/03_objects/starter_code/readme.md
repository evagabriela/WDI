Create an example 'User' object, complete with several 'Meals'.

A 'User' needs to have:

-   a name (`name`)
-   a date-of-birth (`bornOn`)
-   a target daily calorie intake (`calorieTarget`)
-   a list of 'Meals' that they've eaten (`meals`)

Every 'Meal' must have:

-   a title (`title`), e.g. 'breakfast', 'lunch', 'dinner'
-   a date (`date`), represented as a string e.g. "2016-06-25"
-   a description (`description`)
-   a number of estimated calories (`calories`)

Then, create the following methods for your instance of a 'User':

-   `caloriesEatenOn`, which accepts a date (in the format above) and calculates
    the total number of calories consumed on that date.
    
Bonus Tasks -- create the following methods for your instance of a 'User':
-   `avgDailyCalories`, which (as indicated), calculates the average number of
    calories consumed per day, rounded down to the nearest whole calorie.
-   `onTrack`, which compares averageDailyCalories to the User's target daily
    calorie intake, and returns `true` if average caloric intake is at or below
    the target (or `false` if the reverse is true).