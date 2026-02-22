import csv

input_file = "raw_data.csv"
output_file = "cleaned_data.csv"

with open(input_file, newline="") as infile, open(output_file, "w", newline="") as outfile:

    reader = csv.DictReader(infile)
    writer = csv.writer(outfile)

    # Write header once
    writer.writerow(["name", "age", "city", "score"])

    for row in reader:

        # Step 1: Trim whitespace from all fields
        name  = row["name"].strip()
        age   = row["age"].strip()
        city  = row["city"].strip()
        score = row["score"].strip()

        # Step 2: Standardize capitalization
        name = name.capitalize()
        city = city.capitalize()

        # Step 3 & 4: Validate numeric columns — skip row if invalid or missing
        try:
            age   = int(age)
            score = int(score)
        except:
            continue

        # Write the cleaned, valid row
        writer.writerow([name, age, city, score])

print("Done! cleaned_data.csv has been created.")
