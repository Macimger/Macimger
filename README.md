import sqlite3

# Crear o conectar a la base de datos
conexion = sqlite3.connect('jose_maria_vargas.db')

# Crear un cursor
cursor = conexion.cursor()

# Crear tabla Hogares_patria
#cursor.execute('''CREATE TABLE Hogares_patria (
#                    cedula INTEGER PRIMARY KEY,
#                    nombres TEXT,
#                    edad INTEGER,
#                    sexo TEXT,
#                    talla REAL,
#                    peso REAL,
#                   estado_civil TEXT,
#                    profesion TEXT,
#                    ingresos REAL,
#                    direccion TEXT,
#                    beneficio TEXT,
#                    observacion TEXT
#                )''')

# Crear tabla Adulto_mayor
#cursor.execute('''CREATE TABLE Adulto_mayor (
#                    cedula INTEGER PRIMARY KEY,
#                    nombres TEXT,
#                    apellidos TEXT,
#                    edad INTEGER,
#                    sexo TEXT,
#                    talla REAL,
#                    peso REAL,
#                    estado_civil TEXT,
#                    profesion TEXT,
#                    ingresos REAL,
#                    direccion TEXT,
#                    beneficio TEXT,
#                    observacion TEXT
#                )''')

# Crear tabla J_gregorio_hernandez
#cursor.execute('''CREATE TABLE J_gregorio_hernandez (
#                    cedula INTEGER PRIMARY KEY,
#                    nombres TEXT,
#                    apellidos TEXT,
#                    edad INTEGER,
#                    sexo TEXT,
#                    talla REAL,
#                    peso REAL,
#                    estado_civil TEXT,
#                    profesion TEXT,
#                    ingresos REAL,
#                    direccion TEXT,
#                    beneficio TEXT,
#                    observacion TEXT
#                )''')

# Crear tabla Parto_humanizado
#cursor.execute('''CREATE TABLE Parto_humanizado (
#                    cedula INTEGER PRIMARY KEY,
#                    nombres TEXT,
#                    apellidos TEXT,
#                    edad INTEGER,
#                    sexo TEXT,
#                    talla REAL,
#                    peso REAL,
#                    estado_civil TEXT,
#                    profesion TEXT,
#                    ingresos REAL,
#                    direccion TEXT,
#                    beneficio TEXT,
#                    observacion TEXT
#                )''')

# Crear tabla Lactancia_materna
#cursor.execute('''CREATE TABLE Lactancia_materna (
#                    nombres TEXT,
#                    apellidos TEXT,
#                    edad INTEGER,
#                    sexo TEXT,
#                    talla REAL,
#                    peso REAL,
#                    estado_civil TEXT,
#                    profesion TEXT,
#                    ingresos REAL,
#                    direccion TEXT,
#                    beneficio TEXT,
#                    observacion TEXT
#                )''')

# Crear tabla Clap
#cursor.execute('''CREATE TABLE Clap (
#                    cedula INTEGER PRIMARY KEY,
#                    nombres TEXT,
#                    apellidos TEXT,
#                    edad INTEGER,
#                    sexo TEXT,
#                    talla REAL,
#                    peso REAL,
#                    estado_civil TEXT,
#                    profesion TEXT,
#                    ingresos REAL,
#                    direccion TEXT,
#                    beneficio TEXT,
#                    observacion TEXT
#                )''')

# Crear tabla Escolarizacion
#cursor.execute('''CREATE TABLE Escolarizacion (
#                    cedula INTEGER PRIMARY KEY,
#                    nombres TEXT,
#                    apellidos TEXT,
#                    edad INTEGER,
#                    sexo TEXT,
#                    talla REAL,
#                    peso REAL,
#                    estado_civil TEXT,
#                    profesion TEXT,
#                    ingresos REAL,
#                    direccion TEXT,
#                    beneficio TEXT,
#                    observacion TEXT
#                )''')

# Crear tabla lista_de_Estudiantes
#cursor.execute('''CREATE TABLE lista_de_Estudiantes (
#                    cedula INTEGER PRIMARY KEY,
#                    nombres TEXT,
#                    apellidos TEXT,
#                    edad INTEGER,
#                    sexo TEXT,
#                    talla REAL,
#                    peso REAL,
#                    estado_civil TEXT,
#                    profesion TEXT,
#                    ingresos REAL,
#                    direccion TEXT,
#                    beneficio TEXT,
#                    observacion TEXT
#                )''')


cursor.execute("INSERT INTO  hogares_patria VALUES(18687315, willians, castillo, 37, masculino, 1.74, 92.200, soltero, ingeniero, 500.30, calle_san_isidro, hogares, ninguna ) ")

hogares_patria=([
        ("18687315, willians, castillo, 37, masculino, 1.74, 92.200, soltero, ingeniero, 500.30, calle_san_isidro, hogares, ninguna" ) 
        ])

cursor.executemany("INSERT INTO  hogares_patria VALUES (?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?, ?)", hogares_patria)


# Confirmar los cambios
conexion.commit()

# Cerrar la conexión
conexion.close()
