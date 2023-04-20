# Quarterback-Rating-Calculator
This is a quarterback rating calculator, written in Python.

passes_completed = int(input("Enter the amount of passes completed: "))
passes_attempted = int(input("Enter the amount of passes attempted: "))
percentage_completions_per_attempt = (
  (passes_completed / passes_attempted) * 100 - 30) * .05
print("The rating in the percentage of completions per attempt category is", percentage_completions_per_attempt)
passing_yards = int(input("Enter the amount of passing yards: "))
yards_gained_per_attempt = (passing_yards / passes_attempted - 3) * .25
print("The rating in the yards gained per attempt category is", yards_gained_per_attempt)
touchdown_passes = int(input("Enter the amount of touchdown passes: "))
percentage_touchdown_passes_per_attempt = ((touchdown_passes / passes_attempted) * 100) * .2
print("The rating in the percentage of touchdown passes per attempt category is", percentage_touchdown_passes_per_attempt)
interceptions = int(input("Enter the amount of interceptions: "))
percentage_interceptions_per_attempt = 2.375 - (interceptions /                        passes_attempted) * (.25) * (100)
if percentage_interceptions_per_attempt >= 9.5:
  print("The rating in the percentage of interceptions per attempt category is zero")
else:
  print("The rating in the percentage of interceptions per attempt category is", percentage_interceptions_per_attempt)
qb_rating = (percentage_completions_per_attempt + yards_gained_per_attempt + percentage_touchdown_passes_per_attempt + percentage_interceptions_per_attempt) / 6 * 100
print("The quarterback rating is", qb_rating)
