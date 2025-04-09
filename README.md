# Student Feedback System

This is a simple command-line application for collecting student feedback. The application prompts students to enter their name, student ID, and feedback, which is then saved to a text file for later review.

## Features

- Collects student name and ID.
- Allows students to provide feedback.
- Saves feedback entries to a text file (`student_feedback.txt`).
- Simple and easy-to-use command-line interface.

## Requirements

- Python 3.x

## Installation

1. **Clone the repository** (if applicable) or download the `student_feedback.py` file.
   
   ```bash
   git clone <repository-url>
   cd <repository-directory>




   # Student Score Calculator

This is a simple command-line application for calculating the average score of a student based on their input scores. The application prompts the user to enter the number of scores they want to input, collects those scores, and then calculates and displays the average.

## Features

- Prompts the user to enter the number of scores.
- Collects individual scores from the user.
- Validates input to ensure scores are non-negative numbers.
- Calculates and displays the average score.

## Requirements

- Python 3.x

## Installation

1. **Clone the repository** (if applicable) or download the `score_calculator.py` file.
   
   ```bash
   git clone <repository-url>
   cd <repository-directory>




version 1.0.1 
# Feedback Summary Tool

This is a simple command-line application for summarizing student feedback collected from a text file. The application reads feedback entries from `student_feedback.txt`, calculates the total number of entries, and displays each feedback message.

## Features

- Reads feedback from a specified text file (`student_feedback.txt`).
- Calculates the total number of feedback entries.
- Displays each feedback message in a user-friendly format.

## Requirements

- Python 3.x

## Installation

1. **Clone the repository** (if applicable) or download the `feedback_summary.py` file.
   
   ```bash
   git clone <repository-url>
   cd <repository-directory>


def read_feedback(file_path):
    """Read feedback from the specified file."""
    try:
        with open(file_path, 'r') as file:
            feedback_lines = file.readlines()
        return feedback_lines
    except FileNotFoundError:
        print(f"Error: The file '{file_path}' does not exist.")
        return []

def search_feedback(feedback_lines, student_name):
    """Search for feedback entries by student name."""
    matching_feedback = []
    for line in feedback_lines[1:]:  # Skip the header
        if student_name.lower() in line.lower():  # Case-insensitive search
            matching_feedback.append(line.strip())
    return matching_feedback

def display_feedback(matching_feedback):
    """Display the matching feedback entries."""
    if matching_feedback:
        print("\nMatching Feedback Entries:")
        for feedback in matching_feedback:
            print(f"- {feedback}")
    else:
        print("No feedback found for the specified student.")

def main():
    input_file_path = "student_feedback.txt"
    feedback_lines = read_feedback(input_file_path)
    
    if feedback_lines:
        student_name = input("Enter the student's name to search for feedback: ")
        matching_feedback = search_feedback(feedback_lines, student_name)
        display_feedback(matching_feedback)

if __name__ == "__main__":
    main()



# Feedback Management System

This is a simple command-line application for managing student feedback. The application allows users to collect, summarize, search, and count feedback entries. It also provides functionality to export feedback to a text file and generate reports.

## Features

- **Collect Feedback**: Users can enter feedback for students, which is saved to a text file.
- **Summarize Feedback**: Summarizes the total number of feedback entries and lists all feedback messages.
- **Search Feedback**: Allows users to search for feedback entries by student name.
- **Count Feedback**: Counts the total number of feedback entries submitted.
- **Export Feedback**: Users can export feedback entries to a specified `.txt` file.
- **Generate Reports**: Generates a formatted report of feedback entries and saves it to a new text file.

## Installation

1. **Clone the repository** (if applicable) or download the files.
   
   ```bash
   git clone <repository-url>
   cd <repository-directory>
