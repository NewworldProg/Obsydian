views.py
# -------------------
# neka moja funkcionalnost
# ------------------

from django.http import HttpResponse

def provera(request):
    if request.method == "POST":
        return HttpResponse("Kliknuli ste na dugme (POST)")
    return HttpResponse("Ovo je stranica sa GET zahtevom")

			+
urls.py

from . import views

urlpatterns = [
    # ... postojeće rute
    path('provera/', views.provera, name='provera'),
]

			+

template.html

<form method="get" action="{% url 'provera' %}">
    <button type="submit">Klikni ovde (GET)</button>
</form>

ili bezbednije

<form method="post" action="{% url 'provera' %}">
    {% csrf_token %}
    <button type="submit">Klikni ovde (POST)</button>
</form>
crf token se uvek stavlja pre submita, pre nego sto mu nesto vracas, neku info