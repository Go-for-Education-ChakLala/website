---
layout: home
title: Home
---

{% include carousel.html height="66" unit="%" duration="7" number="1" name="home" %}

## Was ist GfE-Chaklala?

GfE-Chaklala ist eine Organisation mit drei Zielen:

1. Förderung und Unterstützung der Christian Cambridge School in Chaklala
2. Förderung von Frauen in der Nähe von Toba Tek Singh in Basismedizin
3. Schulung von örtlichen Pastoren verschiedener christlicher Denominationen

## Wo arbeiten wir?

Christliche Kirchen mit denen wir Kontakt haben sind in **Chaklala, Barakao, Rawat** sowie auf den Dörfern in der Nähe von **Toba Tek Singh.** Dort bieten wir Weiterbildung für Pastoren an.

<div class="grid-card">
	<div class="card">
   	<div id="mapSchool"></div>
   	<script type="text/javascript">
      const mapSchool = new maplibregl.Map({
        container: 'mapSchool',
        style: 'https://tiles.stadiamaps.com/styles/alidade_smooth.json',
        center: [73.11538565889549, 33.59703148873081],
        zoom: 13
      });
      maplibregl.setRTLTextPlugin('https://unpkg.com/@mapbox/mapbox-gl-rtl-text@0.2.3/mapbox-gl-rtl-text.min.js');
      mapSchool.addControl(new maplibregl.NavigationControl());
      const markerCollectionSchool = {
        "type": "FeatureCollection",
        "features": [
          {
            "type": "Feature",
            "geometry": {
              "type": "Point",
              "coordinates": [73.11538565889549, 33.59703148873081]
            },
            "properties": {
              "title": "Christian Cambridge School"
            }
          }
        ]
      };
      markerCollectionSchool.features.forEach((point) => {
        const elem = document.createElement('div');
        elem.className = 'marker';
        const marker = new maplibregl.Marker(elem);
        marker.setLngLat(point.geometry.coordinates);
        const popup = new maplibregl.Popup({ offset: 24, closeButton: false });
        popup.setHTML('<div>' + point.properties.title + '</div>');
        marker.setPopup(popup);
        marker.addTo(mapSchool);
      });
    </script>
    <p>Die Christian Cambridge School ist in <strong>Chaklala</strong>, einer Stadt im Grossraum <strong>Rawalpindi.</strong></p>
	</div>
	<div class="card">
	  <div id="mapVillage"></div>
    <script type="text/javascript">
      const mapVillage = new maplibregl.Map({
        container: 'mapVillage',
        style: 'https://tiles.stadiamaps.com/styles/alidade_smooth.json',
        center: [72.52149251829657, 31.021326843562978],
        zoom: 13
      });
      mapVillage.addControl(new maplibregl.NavigationControl());
      const markerCollectioVillage = {
        "type": "FeatureCollection",
        "features": [{
          "type": "Feature",
          "geometry": {
            "type": "Point",
            "coordinates": [72.52149251829657, 31.021326843562978]
          },
          "properties": {
            "title": "Toba Tek Singh"
          }
        }]
      };
      markerCollectioVillage.features.forEach((point) => {
        var elem = document.createElement('div');
        elem.className = 'marker';
        var marker = new maplibregl.Marker(elem);
        marker.setLngLat(point.geometry.coordinates);
        var popup = new maplibregl.Popup({ offset: 24, closeButton: false });
        popup.setHTML('<div>' + point.properties.title + '</div>');
        marker.setPopup(popup);
        marker.addTo(mapVillage);
      });
    </script>
		<p>Dr. Claire Ebeling arbeitet mit Frauen in einem Dorf in der Nähe von <strong>Toba Tek Singh</strong> im <strong>Punjab.</strong></p>
	</div>
</div>
<br>
## Wie kann ich helfen?

<div class="grid-card">
	<div class="card">
		<img class="card-image" src="assets/images/kontakt.png" />
		<h3>Kontakt</h3>
		<p>
		Lindenweg 10<br>
		CH-8599 Salmsach<br>
		info@gfe-chaklala.org
		</p>
	</div>
	<div class="card">
		<img class="card-image" src="assets/images/give-love.png" />
		<h3>Spenden</h3>
		<p>
			GFE-ChakLala (Go for Education ChakLala)
			<br>
			<br>
			Raiffeisenbank Neukirch-Romanshorn
			IBAN: CH38 8080 8004 8798 7299 5
			<br>
			oder:
			<br>
			Volksbank Mittelhessen e.G.
			IBAN: DE87513900000028717105
			<br>
			<br>
			Vermerk: GfE
		</p>
	</div>
</div>
<br>

<script>
  if (window.netlifyIdentity) {
	window.netlifyIdentity.on("init", user => {
	  if (!user) {
		window.netlifyIdentity.on("login", () => {
		  document.location.href = "/admin/";
		});
	  }
	});
  }
</script>
