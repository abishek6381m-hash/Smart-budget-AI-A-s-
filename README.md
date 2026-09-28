def budget_assistant():
    print("=" * 50)
    print("   SMART AI BUDGET & RECOMMENDATION ASSISTANT")
    print("=" * 50)

    income = float(input("Enter your monthly income: ₹"))

    food = float(input("Enter food expenses: ₹"))
    travel = float(input("Enter travel expenses: ₹"))
    education = float(input("Enter education expenses: ₹"))
    shopping = float(input("Enter shopping expenses: ₹"))
    other = float(input("Enter other expenses: ₹"))

    total_expenses = food + travel + education + shopping + other
    balance = income - total_expenses

    print("\n----- BUDGET SUMMARY -----")
    print(f"Monthly Income     : ₹{income:.2f}")
    print(f"Total Expenses     : ₹{total_expenses:.2f}")
    print(f"Remaining Balance  : ₹{balance:.2f}")

    print("\n----- AI RECOMMENDATION -----")

    if balance < 0:
        print("⚠️ You are spending more than your income.")
        print("Recommendation: Reduce shopping and other unnecessary expenses.")

    elif balance < income * 0.10:
        print("⚠️ Your savings are low.")
        print("Recommendation: Try to save at least 10% of your income.")

    elif balance < income * 0.20:
        print("✓ Your budget is manageable.")
        print("Recommendation: Reduce unnecessary expenses and increase savings.")

    else:
        print("✓ Your budget is healthy.")
        print("Recommendation: Keep your spending controlled and save regularly.")

    print("\n----- SAVINGS PLAN -----")
    recommended_saving = income * 0.20
    print(f"Recommended monthly saving: ₹{recommended_saving:.2f}")

    print("\nThank you for using Smart AI Budget Assistant!")


budget_assistant()
