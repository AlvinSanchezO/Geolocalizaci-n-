# 🌍 GeoMike - Ubicaciones Inteligentes

Aplicación web de geolocalización construida con **Django** y **Django REST Framework**. Permite registrar empleados con sus ubicaciones y resolverlas automáticamente a direcciones reales mediante geocodificación inversa.

---

## Tecnologías

- Python / Django 6
- Django REST Framework
- Geopy (Nominatim)
- TailwindCSS
- SQLite3
- Font Awesome

---

## Estructura del proyecto

```
crispy-enigma/
├── core_main_geomike/      # Configuración principal del proyecto
├── admin_geomike/          # App principal (modelos + vista frontend)
│   ├── models.py           # Modelos: Empleado, Direccion
│   └── views.py            # Vista home (renderiza index.html)
├── core_api/               # API REST
│   ├── Serializers/        # EmpleadoSerializer
│   ├── Viewsets/           # EmpleadoViewSet (CRUD)
│   └── routers.py          # Router DRF
├── Herramientas/
│   └── get_direccion_mike.py  # Geocodificación inversa con geopy
└── templates/
    └── index.html          # Frontend completo (Tailwind + JS)
```

---

## Instalación

```bash
# 1. Clonar el repositorio
git clone https://github.com/AlvinSanchezO/Geolocalizaci-n-.git
cd Geolocalizaci-n-

# 2. Crear y activar entorno virtual
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # Linux/Mac

# 3. Instalar dependencias
pip install -r requierements.txt

# 4. Aplicar migraciones
python manage.py migrate

# 5. Crear superusuario (opcional)
python manage.py createsuperuser

# 6. Ejecutar el servidor
python manage.py runserver
```

---

## Endpoints

| Método | URL | Descripción |
|--------|-----|-------------|
| GET | `/` | Frontend principal |
| GET/POST | `/api-mike/empleados/` | Listar / crear empleados |
| GET/PUT/DELETE | `/api-mike/empleados/{id}/` | Detalle / editar / eliminar empleado |
| GET | `/api-auth/` | Autenticación DRF (browsable API) |
| GET | `/admin/` | Panel de administración Django |

---

## Funcionalidades

- Detección de ubicación del usuario vía navegador (Geolocation API)
- Geocodificación inversa automática al guardar una `Direccion`
- API REST completa para gestión de empleados
- Frontend responsivo con tarjetas de ubicaciones destacadas

---


