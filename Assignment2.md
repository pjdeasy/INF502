def pythagoreanTheorem(length_a,length_b):
    pythagoreanTheorem =sqrt( length_a**2 + length_b**2)
    return pythagoreanTheorem
pythagoreanTheorem(2,2)
2.8284271247461903
pythagoreanTheorem(3,3)
4.242640687119285
pythagoreanTheorem(3,4)
5.0

##########################################################################

def list_mangler(list_in):
    nbr=[]
    for number in list_in:
        if number%2 == 0:
            nbr.append(number*2)
        else:
            nbr.append(number*3)
    return nbr

list_mangler([1, 2, 3, 4])

##########################################################################


##########################################################################

def odd_even_filter(nbrs):
    even = []
    odd = []
    for i in nbrs:
        if i % 2 == 0:
            even.append(i)
        else:
            odd.append(i)
    return [even, odd]

odd_even_filter([1, 2, 3, 4, 5, 6, 7, 8, 9])

#############################################################################
def grade_calc(grades_in, to_drop):
    grades_in= []
    to_drop = to_drop
    for i in sorted(grade_calc):
        grades_in.remove[0:n]
    return grades_in

grade_calc([100,90,80],2)

score = (sum(grades_in) - min(grades_in)) / (len(grades_in) - to_drop)

def determinGrade (avgScore):
    if ( avgScore <60 ):
        return "F"
    elif( avgScore <70 ):
        return "D"
    elif( avgScore <80 ):
        return "C"
    elif( avgScore <90 ):
        return "B"
    elif( avgScore <101 ):
        return "A"
