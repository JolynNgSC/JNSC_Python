# Python Pratice 
## Objective
The following attempts were made to self-learn python.

### While and For Loop 

### If / Elif Statements

# Activity 1

"I am tasked to write a python code that converts time to a 24 hour clock using if/elif."

    time = int(input("Enter the time: "))
    if time < 0 or time > 24:
        print("Invalid time entered.")
    elif time <= 12:
        print("The time conversion is " + str(time) + " AM")
        time_2 = time + 12
        print("In the afternoon, it would be " + str(time_2) + " PM")
    else:
        time_3 = time - 12
        print("The time conversion is " + str(time_3) + " PM")
        time_4 = time_3 - 12
        print("In the morning, it would be " + str(time_4) + " AM")

Any input that are lesses than 0 (-1, -2...) or greater than 24 (25, 26....) an 'Invalid Time Entered' input will be placed. 
Else and If the input time is less than or equal 12, a + 12 will be added to determine the PM while nothing will determine AM. 
While, if the time is greater than 12, it would be subjected to a - 12 to determine the PM. Another - 12 would be used to
determine the AM. 


# Activity 2

"I am tasked to write a python code that converts dollar values between SGD and USD."

    def sgd_to_usd(amount):
        return amount * 0.73
    def usd_to_sgd(amount):
        return amount * 1.36
    
    currency = input("Enter 'SGD' for Singapore Dollars to US Dollars conversion, or 'USD' for US Dollars to Singapore Dollars conversion: ")
    amount = float(input("Enter the amount: "))
    
    if currency.upper() == 'SGD':
        converted_amount = sgd_to_usd(amount)
        print(f"{amount} SGD is equal to {converted_amount} USD.")
    elif currency.upper() == 'USD':
        converted_amount = usd_to_sgd(amount)
        print(f"{amount} USD is equal to {converted_amount} SGD.")
    else:
        print("Invalid currency choice. Please enter 'SGD' or 'USD'.")

Firstly, we defined the return amount for SGD and USD to ease the calculation later. We created an input asking for an answer 
which was named currency. The currency conversion would then be paired with an ammount. So using if/elif statement, we included 
that any ammount given be it in SGD or USD, will be subjected to the calulcation. The .upper was used because we want it to be 
in case-insensitive, hence it would read in both lower and upper case.

So, what are we looking for:

    if ammount = value, value would multiply by the conversion rate.
    
    ammount = 15                                       amount = 20
    currency = SGD                                     currency = USD
    
    total = 15 * Defined SGD (0.73)                    total = 20 * Defined USD (1.36)

