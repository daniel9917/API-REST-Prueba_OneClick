# API-REST-Prueba_OneClick

There are six endpoints.

Registro	POST	/autor/create
Request Body be like:
{
    "nombre" : "jose",
    "fecha_nacimiento" : "17/08/1999",
    "ciudad_procedencia" : "bogotá",
    "correo" : "daniel.jose.45@hotmail.com"
}


Listado	GET	/autor/find
Response Body example:
[
    {
        "id": 7,
        "nombre": "jose",
        "fecha_nacimiento": "bogotá",
        "ciudad_procedencia": "daniel.jose.45@hotmail.com",
        "correo": "17/08/1999",
        "libros": [
            {
                "id": 12,
                "titulo": "fefe",
                "ano": "2021",
                "n_paginas": 500,
                "editorial_id": null,
                "autor_id": null,
                "genero": "comedia"
            }
        ]
    }
]

Registro	POST	/libro/create
Request Body example:
{
    "titulo" : "fefe",
    "ano" : "2021",
    "genero" : "comedia",
    "n_paginas" : 500,
    "id_editorial" : 10,
    "id_autor" : 7
}



Listado	GET	/editorial/find
Response Body example:
[
    {
        "id": 8,
        "nombre": "babel",
        "direccion": "Calle 39 A 20 - 55",
        "telefono": "245 8495",
        "correo": "editorial@babellibros.com.co",
        "max_libros": 0,
        "libros": [
            {
                "id": 12,
                "titulo": "fefe",
                "ano": "2021",
                "n_paginas": 500,
                "editorial_id": null,
                "autor_id": null,
                "genero": "comedia"
            }
        ]
    }
]


Registro	POST	/editorial/create
Request Body example:
{
    "nombre" : "babel",
    "direccion" : "Calle 39 A 20 - 55",
    "correo" : "editorial@babellibros.com.co",
    "telefono" : "245 8495"    
}



Listado	GET	/libro/find
Response body example:
[
    {
        "id": 12,
        "titulo": "fefe",
        "ano": "2021",
        "n_paginas": 500,
        "editorial_id": 8,
        "autor_id": 7,
        "genero": "comedia"
    }
]

