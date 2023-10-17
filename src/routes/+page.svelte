<script lang="ts">
	import Conctacts from '$lib/components/Conctacts.svelte';
	import Hero from '$lib/components/Hero.svelte';
	import Part from '$lib/components/Part.svelte';
	import Produits from '$lib/components/Produits.svelte';
	import Quality from '$lib/components/Quality.svelte';
	import Services from '$lib/components/Services.svelte';
	import About from '$lib/components/about.svelte';
</script>

<svelte:head>
	<meta
		name="description"
		content="Bienvenue sur notre page d’accueil, où nous sommes votre partenaire de confiance dans la fourniture de matériaux d’automatisation pour les portails, portes de garage, ascenseurs, portes piétonnes automatiques et pièces détachées. Découvrez notre large gamme de produits fiables et de haute qualité conçus pour améliorer la commodité, la sécurité et l’efficacité. Que vous soyez propriétaire d’une maison, propriétaire d’une entreprise ou professionnel de l’industrie, nous avons les solutions d’automatisation dont vous avez besoin. Collaborez avec nous et découvrez l’intégration transparente de la technologie de pointe et du savoir-faire supérieur situe a Abidjan Cote d'ivoire"
	/>
	<title>yvenos service</title>
</svelte:head>

<Hero />
<About />
<Quality />
<Part />
<Produits />
<Services />
<Conctacts />
