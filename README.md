print("Welcome to the quiz program!")
name = input("What's your name? ")
print(f"Hello, {name}! Let's start the quiz.\n")

score = 0

questions = [
    {
        "question": 'What will len("hello") return?',
        "options": ["4", "5", "8", "2"],
        "answer": "B"
    },
    {
        "question": "Which data type stores text?",
        "options": ["str", "int", "bool", "float"],
        "answer": "A"
    },
    {
        "question": "What does CPU stand for?",
        "options": ["central processing unit", "computer power unit", "computer processing unit", "central power unit"],
        "answer": "A"
    },
    {
        "question": "What is the output of print(2**3)?",
        "options": ["6", "8", "5", "9"],
        "answer": "B"
    },
    {
        "question": "What is 2 × 5?",
        "options": ["10", "15", "7", "5"],
        "answer": "A"
    }
]

for i, q in enumerate(questions, start=1):
    print(f"\nQuestion {i}: {q['question']}")
    for idx, option in zip("ABCD", q['options']):
        print(f"{idx}) {option}")
    user_answer = input("Choose your answer (A/B/C/D): ").strip().upper()

    if user_answer == q["answer"]:
        score += 1
    else:
        print(f"Sorry, the correct answer is {q['answer']}")

print(f"\nQuiz over, {name}! Your final score is {score} out of {len(questions)}")
