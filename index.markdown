---
layout: home
title: Home
carousels:
    - images:
        - image: assets/images/carousel-1.jpg
        - image: assets/images/carousel-2.jpg
        - image: assets/images/carousel-3.jpg
        - image: assets/images/carousel-4.jpg
        - image: assets/images/carousel-5.jpg
        - image: assets/images/carousel-6.jpg
---

{% include carousel.html height="66" unit="%" duration="7" number="1" %}

## Was ist GfE-Chaklala?

GfE-Chaklala ist eine Organisation mit drei Zielen:

1. Förderung und Unterstützung der Christian Cambridge School in Chaklala
2. Förderung von Frauen in der Nähe von Toba Tek Singh in Basismedizin
3. Schulung von örtlichen Pastoren verschiedener christlicher Denominationen

## Wo arbeiten wir?

Christliche Kirchen mit denen wir Kontakt haben sind in **Chaklala, Barakao, Rawat** sowie auf den Dörfern in der Nähe von **Toba Tek Singh.** Dort bieten wir Weiterbildung für Pastoren an.

<div class="grid-card">
	<div class="card">
		{% google_map width="100%" latitude="33.59703148873081" longitude="73.11538565889549" marker_title="Horizon School Chaklala"%}
		<p>Die Christian Cambridge School ist in <strong>Chaklala</strong>, einer Stadt im Grossraum <strong>Rawalpindi.</strong></p>
	</div>
	<div class="card">
		{% google_map width="100%" latitude="31.021326843562978" longitude="72.52149251829657" marker_title="Toba Tek Singh"%}
		<p>Dr. Claire Ebeling arbeitet mit Frauen in einem Dorf in der Nähe von <strong>Toba Tek Singh</strong> im <strong>Punjab.</strong></p>
	</div>
</div>
<br>
## Wie kann ich helfen?

<div class="grid-card">
	<div class="card info-card">
		<div class="card-image">
			<img src="assets/images/kontakt.png" />
		</div>
		<h3>Kontakt</h3>
		<p>
		Lindenweg 10<br>
		CH-8599 Salmsach<br>
		info@gfe-chaklala.org
		</p>
	</div>
	<div class="card info-card">
		<div class="card-image">
			<img src="assets/images/give-love.png" />
		</div>
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
