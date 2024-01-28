def cat_age_to_human_years(cat_age):
    if cat_age < 0:
        raise ValueError("Cat's age must be a non-negative integer.")
    
    if cat_age == 1:
        human_years = 15
    elif cat_age == 2:
        human_years = 24
    else:
        human_years = 24 + (cat_age - 2) * 4
    
    return human_years

def get_valid_cat_age():
    while True:
        try:
            cat_age = int(input("Enter your cat's age in cat years: "))
            if cat_age < 0:
                raise ValueError("Cat's age must be a non-negative integer.")
            return cat_age
        except ValueError:
            print("Invalid input. Please enter a valid non-negative integer for the cat's age.")

# Example usage:
try:
    cat_age = get_valid_cat_age()
    human_years = cat_age_to_human_years(cat_age)
    print(f"Your cat's age in human years is approximately {human_years} years.")
except ValueError as e:
    print(f"Error: {e}")
