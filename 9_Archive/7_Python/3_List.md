lst = [1, 2, 3]
del lst[0]
print(lst) # выведет [2, 3]

lst = [1, 2, 3]
lst.remove(1) # ! если два совпадения удалится только первое
print(lst) # выведет [2, 3]

lst1 = [1, 2, 3]
lst2 = [4, 5, 6]
res = lst1 + lst2
print(res) # выведет [1, 2, 3, 4, 5, 6]

lst = [1, 2, 3]
res = 1 in lst
print(res) # выведет True



### МЕТОДЫ 
lst = ['a', 'b', 'c']
lst.append('d') # добавит элемент в конец
print(lst) # выведет ['a', 'b', 'c', 'd']

lst1 = [1, 2, 3]
lst2 = [4, 5, 6]
lst1.extend(lst2) # объединит первый список со вторым
print(lst1) # выведет [1, 2, 3, 4, 5, 6]

lst = ['a', 'b', 'c', 'd']
lst.insert(1, '2') # вставит на указанный индекс новое значение, подвинув все остальные значения вперед
print(lst) # выведет ['a', '2', 'b', 'c', 'd']

lst = [1, 2, 3]
print(lst.pop(0)) # удалит элемент по индексу и выведет его = 1
print(lst) # выведет [2, 3]

lst = [1, 2, 3]
lst.clear() # удаление всех элементов
print(lst) # выведет []

lst = [1, 2, 3]
print(lst.index(1)) # выведет 0

lst = [1, 2, 1, 3]
print(lst.count()) # выведет 4
print(lst.count(1)) # выведет 2

lst = [1, 2, 3]
lst.reverse() # перевернет список
print(lst) # выведет [3, 2, 1]

lst = [3, 2, 1]
lst.sort()
print(lst) # выведет [1, 2, 3]
lst.sort(reverse=True)
print(lst) # выведет [3, 2, 1]