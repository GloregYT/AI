# AI

result = []


def divider(a, b):

    if a < b:
    
        raise ValueError("a is less than b")
    if b > 100:

        raise IndexError("b is greater than 100")
        
    return a / b

data = {10: 2, 2: 5, "123": 4, 18: 0, 8: 4}  # Прибрано некоректний ключ []

for key in data:

    try:
    
        res = divider(int(key), data[key])  # Додано конвертацію ключа до int
        
        result.append(res)
        
    except ZeroDivisionError:
    
        print(f"Error: Division by zero for key {key}.")
        
    except ValueError as e:
    
        print(f"ValueError: {e} for key {key}.")
        
    except IndexError as e:
    
        print(f"IndexError: {e} for key {key}.")
        
    except TypeError as e:
    
        print(f"TypeError: {e} for key {key}.")
        
    except Exception as e:  # Загальний виняток для інших випадків
    
        print(f"Unexpected error {type(e).__name__}: {e} for key {key}.")

print(result)


ValueError: a is less than b for key 2. / 
Error: Division by zero for key 18. / 
[5.0, 30.75, 2.0]
