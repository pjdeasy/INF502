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

def grade_calc(grades_in,to_drop):
    to_drop=to_drop
    grade_calc_lst = sorted(grades_in)[to_drop:]
    grades_in=sum(grade_calc_lst) / len(grade_calc_lst)
    if ( grades_in <60 ):
        print('F')
    elif( grades_in <70 ):
        print('D')
    elif( grades_in <80 ):
        print('C')
    elif( grades_in <90 ):
        print('B')
    elif( grades_in <101 ):
        print('A')

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
