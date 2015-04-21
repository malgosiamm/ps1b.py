# Problem Set 2
# Name: Małgorzata Metryka
# Collaborators: Natalia Prósińska
# Time Spent: 4h



initialBal = float(input("Enter the outstanding balance on your credit card: "))
interestRate = float(input("Enter the annual credit card interest rate as a decimal: (as a decimal, i.e. 18% is .18): "))


monthlyPayment = 10
monthlyInterestRate = interestRate/12
bal = initialBal

while bal > 0:

   monthlyPayment += 10
   bal = initialBal
   numMonths = 0

   while numMonths < 12 and bal > 0:

       numMonths += 1

       interest = monthlyInterestRate * bal

       bal -= monthlyPayment

       bal += interest

bal = round(bal,2)


print ('RESULT')
print ('Monthly payment to pay off debt in 1 year:', monthlyPayment)
print ('Number of months needed:', numMonths)
print ('Balance:', bal)
