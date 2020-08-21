# temperature-converter-
def celsiusToFahrenheit(celsius):
    fahrenheit = round(celsius * 1.8 + 32, 3)
    return fahrenheit

def celsiusToKelvin(celsius):
    kelvin = round(celsius + 273.15, 3)
    return kelvin

def kelvinToCelsius(kelvin):
    celsius = round(kelvin - 273.15, 3)
    return celsius

def fahrenheitToCelsius(fahrenheit):
    celsius = round((fahrenheit - 32)/1.8,3)
    return celsius

def main():
    print("Enter value of Temperature:")
    temperature = float(input().strip())
    print("Enter C for Celsius, F for Fahrenheit and K for Kelvin")
    print("Enter From scale: ")
    fromScale = input().strip()
    print("Enter TO scale: ")
    toScale = input().strip()
    
    if(fromScale == toScale):
        print(temperature," ",fromScale)
          
    if(fromScale == "C"):
        tempInCelsius = temperature
    else:
        if(fromScale == "F"):
            tempInCelsius = fahrenheitToCelsius(temperature)
        elif(fromScale == "K"):
            tempInCelsius = kelvinToCelsius(temperature)
        
    if(toScale == "C"):
        print(tempInCelsius," C")
    else:
        if(toScale == "F"):
            print(celsiusToFahrenheit(tempInCelsius)," F")
        elif(toScale == "K"):
            print(celsiusToKelvin(tempInCelsius)," K")
        
if __name__ == "__main__":
    main()
