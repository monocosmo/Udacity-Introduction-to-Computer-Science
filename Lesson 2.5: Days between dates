def DateIsBefore (year1, month1, day1, year2, month2, day2):
    """To make sure the inputs are valid.
       Return True if the Date1 is before Date2."""
    if year1 < year2:
        return True
    if year1 == year2:
        if month1 < month2:
            return True
        if month1 == month2:
            return day1 < day2
    else:
        return False
        
def LeapYear(year):
    if year % 400 == 0:
        return True
    if year % 100 == 0:
        return False
    if year % 4 == 0:
        return True
    else:
        return False

def DaysInMonth(year, month):
    if month == 1 or month == 3 or month == 5 or month == 7 or month == 8 or month == 10 or month == 12:
        return 31
    else:
        if month == 2:
            if LeapYear(year):
                return 29
            else:
                return 28
        else:
            return 30
            
def NextDay(year, month, day):
    if day < DaysInMonth(year, month):
        return year, month, day + 1
    else:
        if month < 12:
            return year, month + 1, 1
        else:
            return year + 1, 1, 1

def DaysBetweenDates(year1, month1, day1, year2, month2, day2):
    if DateIsBefore(year1, month1, day1, year2, month2, day2):
        days = 0
        while DateIsBefore(year1, month1, day1, year2, month2, day2):
            year1, month1, day1 = NextDay(year1, month1, day1)
            days = days + 1
        return days
    else:
        return "Invalid input. The second date should be after the first one."
