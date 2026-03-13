# practica-guia-1
import numpy as np
import pandas as pd

data = {
'Producto':['Laptop', 'Mouse', 'Monitor', 'Teclado'],
'Precio': [750000, 20000, 50000, 35000],
'Stock':[10, 20, 15, 25]
}

df = pd.DataFrame(data)
display(df)
print("\n" + "*"*30 + "\n")

promedio = df["Stock"].mean()
print("el promedio de Stock de los productos es :",promedio)
print("\n" + "*"*30 + "\n")

df_stock = df[df["Stock"] >= 20]
display(df_stock)
print("\n" + "*"*30 + "\n")

promedioPrecio = df["Precio"].mean()
print("el promedio de Precio de los productos es :",promedioPrecio)
print("\n" + "*"*30 + "\n")

total_stock = df["Stock"].sum()
print("El total de Stock de los productos es:", total_stock)
print("\n" + "*"*30 + "\n")

df_precio = df[df["Precio"] >= 500000]
display(df_precio)
print("\n" + "*"*30 + "\n")


#-----------------------------------------------------------------------------------------------------------
import numpy as np
import pandas as pd

#1 lista de datos
notas=[6.5, 7.0, 4.3, 5.1]
print(notas)
print("la primera calificacion es: ",notas[0])
promedio=(notas[0]+ notas[1]+notas[2]+ notas[3])/4
print(f"el promedio de notas es: ")
print("el promedio de notas es:",promedio)

#2 diccionario de datos
notas_estudiantes ={
    "ana": 6.5,
    "luis": 7.0,
    "maria": 4.3,
    "pedro": 5.1
}
print(notas_estudiantes)
promedioD =sum(notas_estudiantes.values())/len(notas_estudiantes)
print(promedioD)



#array
notas_Estudiantes = np.array([6.5, 7.0, 4.3, 5.1])
print(notas_Estudiantes)



#DATA FRAME
datos = {
    "nombre": ["ana","luis","pedro","maria"],
    "nota" : [6.5, 7.0, 4.3, 5.1]
}
df = pd.DataFrame(datos)
print(df)
df
promedio = df["nota"].mean()
print("el promedio notas es: ",promedio)

df_promediobajo = df[df["nota"] < 5.0]
print(df_promediobajo)

df_notaAlta = df[df["nota"] >= 7.0]
print(df_notaAlta)


max_nota = df['nota'].max()
print(f"La nota más alta es: {max_nota}")

df_nota_mas_alta = df.loc[df['nota'] == max_nota]
print("Estudiante(s) con la nota más alta:")
display(df_nota_mas_alta)

