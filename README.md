/* # Actividad-3
Menú áreas de figuras geométricas */

class cuadrado {
  var lado:Double

  init(lado: Double){
    self.lado = lado
  }
    func calcularArea() -> Double {
      return lado * lado
  }
}

class rectangulo {
  var alto: Double
  var largo: Double

  init(alto: Double, largo: Double){
    self.alto = alto
    self.largo = largo
  }

  func calcularArea() -> Double {
    return alto * largo
  }
}

class triangulo {
  var base: Double
  var altura: Double

  init(base: Double, altura: Double){
    self.base = base
    self.altura = altura
  }
  func calcularArea() -> Double {
    return (base * altura)/2
  }  
}

class circulo {
var radio: Double
let pi = 3.14159
  
  init(radio: Double){
    self.radio = radio
  }

  func calcularArea() -> Double {
    return Double.pi * radio * radio
  }
}

var opcion: Int = 0
var bandera = true
repeat {
  print (" °°°°° Menu de opciones para calcular área °°°°°")
  print("                  1. Cuadrado")
  print("                  2. Rectangulo")
  print("                  3. Triangulo")
  print("                  4. Circulo")
  print("                  5. Salir")
  print("")
  print("Introduce el  número de la opcion requerida:")
  let opcion = Int(readLine()!)!
  switch opcion {
    case 1:
      print("Introduce el lado del Cuadrado")
      let xlado = Double(readLine()!)!
      let calculadorDeAreas = cuadrado(lado: xlado)
      print("El área del cuadrado es \(calculadorDeAreas.calcularArea())")
      print("--------------------------------------------")    
      print("")
    case 2:
      print("Introduce el alto del rectangulo")
      let xalto = Double(readLine()!)!
      print("Introduce el largo del rectangulo")
      let xlargo = Double(readLine()!)!
      let calculadorDeAreas = rectangulo(alto: xalto, largo: xlargo)
      print("El área del Rectangulo es \(calculadorDeAreas.calcularArea())")
      print("--------------------------------------------")
      print("")
    case 3:
      print("Introduce la base del Triangulo")
      let xbase = Double(readLine()!)!
      print("Introduce la altura del Triangulo")
      let xaltura = Double(readLine()!)!
      let calculadorDeAreas = triangulo(base: xbase, altura: xaltura)
      print("El área del Triangulo es \(calculadorDeAreas.calcularArea())")
      print("--------------------------------------------")
      print("")
    case 4:
      print("Introduce el Radio del Circulo")
      let xradio = Double(readLine()!)!
      let calculadorDeAreas = circulo(radio: xradio)
      print("El área del Circulo es \(calculadorDeAreas.calcularArea())")
      print("--------------------------------------------")
      print("")
    case 5:
      print ("Salida")
      bandera = false
    default:
      print ("Opcion Invalida")
      print("")
  }
  
}  while bandera == true

