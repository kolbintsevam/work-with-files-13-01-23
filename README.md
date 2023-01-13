cook_book = {}
with open('file1.txt', 'rt', encoding='utf8') as file:
        for d in file:
            dish_name = d.strip()
            cook_book[dish_name] = []
            ingridients_count = file.readline()
            for ingridient in range(int(ingridients_count)):
                ingridient = file.readline()
                ingridient_name, quantity, measure = ingridient.split(' | ')
                ingridients_list = {'ingridient_name': ingridient_name, 'quantity': quantity,
                                    'measure': measure}
            blank_line = file.readline()
            cook_book[dish_name].append(ingridients_list)
print(cook_book)