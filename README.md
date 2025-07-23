1.	def calculate_total_price(cart_items):
    if not cart_items:
        return "Cart is empty."

    total_items = len(cart_items)
    total_price = sum(cart_items.values())

    # Apply 10% discount if more than 5 items
    if total_items > 5:
        discount = total_price * 0.10
        total_price -= discount

    return f"Total Price: {int(total_price)}"

# Example input
cart_items = {
    'Laptop': 50000,
    'Headphones': 2000,
    'Mouse': 500,
    'Keyboard': 1500
}

# Output
print(calculate_total_price(cart_items))







2.	def add_menu_item(menu, item):
    if item not in menu:
        menu.append(item)

def remove_menu_item(menu, item):
    if item in menu:
        menu.remove(item)
    else:
        print(f"Cannot remove '{item}': Item not found in the menu.")

def check_menu_item(menu, item):
    return f"{item} is available" if item in menu else f"{item} is not available"

# Input example
initial_menu = ["Pizza", "Burger", "Pasta", "Salad"]
add_item = "Tacos"
remove_item = "Salad"
check_item = "Pizza"

# Operations
add_menu_item(initial_menu, add_item)
remove_menu_item(initial_menu, remove_item)
availability = check_menu_item(initial_menu, check_item)

# Output
print("Updated menu:", initial_menu)
print("Availability:", availability)




3.	class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def average(self):
        return sum(self.marks) / len(self.marks)

def calculate_averages(student_data):
    averages = {}
    for name, marks in student_data.items():
        student = Student(name, marks)
        avg = round(student.average(), 2)
        averages[name] = avg
    return averages

def find_top_performer(averages):
    return max(averages, key=averages.get)

# Input Example
students = {
    "John": [85, 78, 92],
    "Alice": [88, 79, 95],
    "Bob": [70, 75, 80]
}

# Calculate averages
average_marks = calculate_averages(students)
top_performer = find_top_performer(average_marks)

# Output
print("Average Marks:", average_marks)
print("Top Performer:", top_performer)

4.	def book_seat(booked, seat, total):
    if seat < 1 or seat > total:
        print(f"Seat {seat} is invalid.")
    elif seat in booked:
        print(f"Seat {seat} is already booked.")
    else:
        booked.append(seat)
        print(f"Seat {seat} booked successfully.")

def cancel_seat_booking(booked, seat):
    if seat in booked:
        booked.remove(seat)
        print(f"Seat {seat} cancelled successfully.")
    else:
        print(f"Seat {seat} was not booked.")

def get_available_seats(total, booked):
    return [seat for seat in range(1, total + 1) if seat not in booked]

# Input Example
total_seats = 10
booked_seats = [2, 5, 7]

book_seat_number = 3
cancel_seat_number = 5

# Operations
book_seat(booked_seats,)
5.	# Optional Patient class
class Patient:
    def __init__(self, name, age, disease):
        self.name = name
        self.age = age
        self.disease = disease

    def to_dict(self):
        return {"Name": self.name, "Age": self.age, "Disease": self.disease}

# Function to search for patients by disease
def search_by_disease(patients_list, disease):
    return [patient for patient in patients_list if patient["Disease"].lower() == disease.lower()]

# Input example: List of patient records
patients = [
    {"Name": "Alice", "Age": 30, "Disease": "Flu"},
    {"Name": "Bob", "Age": 45, "Disease": "Diabetes"},
    {"Name": "Charlie", "Age": 35, "Disease": "Flu"}
]

# Example disease to search
search_disease = "Flu"

# Perform the search
matched_patients = search_by_disease(patients, search_disease)

# Output
print(f"Patients with {search_disease}:")
for patient in matched_patients:
    print(patient)
6.	def calculate_positive_feedback(ratings):
    if not ratings:
        return "No ratings available."

    positive_count = sum(1 for r in ratings if r >= 4)
    percentage = (positive_count / len(ratings)) * 100
    return f"Positive Feedback: {round(percentage, 1)}%"

# Input Example
ratings = [5, 4, 3, 5, 2, 4, 1, 5]

# Output
result = calculate_positive_feedback(ratings)
print(result)

7.	# Function to calculate fare for a single trip
def calculate_fare(distance_km):
    base_fare = 50
    distance_fare = 10 * distance_km
    return base_fare + distance_fare

# Input Example
trips = [5, 10, 3]  # Distances in km

# Calculate and display fare for each trip
total_fare = 0
for i, distance in enumerate(trips, start=1):
    fare = calculate_fare(distance)
    total_fare += fare
    print(f"Trip {i}: ${fare}")

# Display total fare
print(f"\nTotal Fare: ${total_fare}")
# -core-python-assignment-
