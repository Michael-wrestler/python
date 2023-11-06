import re
def car_number():
    car_number_1 = str(input ('Введите номер машины: '))
    valid = re.findall ('^[АВЕКМНОРСТУХ]\d{3}(?<!000)[АВЕКМНОРСТУХ]{2}\d{2,3}',car_number_1)
    number = re.findall ('^[АВЕКМНОРСТУХ]\d{3}(?<!000)[АВЕКМНОРСТУХ]{2}',car_number_1)[0]
    region = re.findall ('\d{2,3}$', car_number_1)[0]                   
    if car_number := valid:
        print("Номер",number, "валиден.","Регион: ",region)
    else:
        print("Номер не валиден")
    return car_number_1
car_number()