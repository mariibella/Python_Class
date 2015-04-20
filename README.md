# Python_Class
Group project for Programming in Python - April 2015
import datetime
travel_date=str(input(('Please enter the date of your travel (Date-Month-Year, i.e. 04-Apr-15):')))
try:
    date_object=datetime.datetime.strptime(travel_date,'%d-%b-%y')
except:
    print("Please enter a valid date!")
today=datetime.datetime.now()
now=datetime.datetime.now()
time_until_travel = date_object - today
if date_object <= today:
    print("Apologies, this date is in the past! Please enter a valid date!")
else:
    print("Days until Travel",time_until_travel.days)
    print("Seconds until Travel",time_until_travel.total_seconds())
    print("Minutes until Travel",time_until_travel.total_seconds()/60)
    print("Hours until Travel",time_until_travel.total_seconds()/60/60)
    print("Years until Travel",time_until_travel.days/365)
