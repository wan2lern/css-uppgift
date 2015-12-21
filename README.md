# Uppgift 2 CSS - Tanken bakom designen
### Av Daniel Karjanlahti 2015-12-20-22:00

##Svårigheter
Den största tiden gick åt till att tweaka header delen, och då framförallt media queries. Jag ville skapa en flat design, en enkel och clean design. Den största utmaningen var HTML uppmärkningen, den var så rörig och i helt fel ordning (om man läser innehållet). Jag tar upp det här längre ner i DOM träd avsnittet längre ner.



##Typsnitt
De två font-family jag valde var "Caviar Dreams", en Art Deco font, och det är typsnittet jag använder här, och "Wasted" som är mer kurvig variant, den gav liv åt layouten tyckte jag. Just Art Deco stilen förstärker flat design intrycket ytterligare.
Jag valde att förskjuta paragraferna lite till vänster för att det såg snyggt ut helt enkelt.



##Innehåll
Jag la mycket fokus vid aside .sidebar och fick ommöblera en hel del för att få den att hamna under stycket som nämner den. Jag placerade den därför högt upp. Hela layouten är uppdelad i 5 block; header, .preamble, .summary, .sidebar och så .main som innehåller det mesta. Jag valde att fixera footer som innehåller 5 länkar och en av dom extra div elementen i vilken jag la en färg-stripe, och samma färg-stripe finns även på toppen av sidan. Jag tyckte att dom gav en diskret färgklick till sidan. Jag börjar sidan med The Road to Enlightenment, som börjar med en liten dikt och kändes som en passande start. Därefter kommer uppmaningen att ladda ner CSS och HTML filerna, och uppmaningen att ladda in en stilmall från listan i aside .sidebar som jag gjorde rund för att betona den ytterligare. Jag la även till en hint med ::after. 
Jag ändrade även cursor för abbr till att vara pointer.



##Bilder
Dom två större bilderna jag använde var en CSS3 logo och en jag kallar "Tummen upp". Dessa bilder placerade jag med hjälp av ::after mest för att jag ville testa på att använda det.
När man använder små enheter har jag valt att ta bort bilderna.


##Validering
Jag fick en del varningar på -webkit-flex och -moz-flex eftersom dom inte är vedertagna.


##DOM träd
Min uppfattning var att HTML-koden var så rörigt att jag var tvungen att göra ett DOM-träd av det.
Det fungerar så här; Ju högre siffra, desto djupare in i DOM är det. Man får också en snabb överblick av vilka element som finns i vilken wrapper. Jag gjorde också huvudrubrikerna större så att man lätt ser dom.

<code>
0 body
1 div .page-wrapper
	2 section .intro
		3 header [role=banner]
			4 h1 CSS Zen Garden
			4 h2 The Beauty of CSS Design

		3 div .summary #zen-summary role[article]
			4 p A demonstration of what can be accomplished through CSS-based design. Select any style sheet from the list to load it into this page.
			4 p Download the example html file and css file

		3 div .preamble .zen-preamble role[article]
			4 h3 The Road to Enlightenment
			4 p Littering a dark and dreary road lay the past relics of browser-specific tags, incompatible DOMs, broken CSS support, and abandoned browsers.
			4 p We must clear the mind of the past. Web enlightenment has been achieved thanks to the tireless efforts of folk like the W3C, WaSP, and the major browser creators.
			4 p The CSS Zen Garden invites you to relax and meditate on the important lessons of the masters. Begin to see with clarity. Learn to use the time-honored techniques in new and invigorating fashion. Become one with the web.

	2 div .main .supporting #zen-supporting role[main]
		3 div .explanation .zen-explanation role[article]
			4 h3 So What is This About?
			4 p There is a continuing need to show the power of CSS. The Zen Garden aims to excite, inspire, and encourage participation. To begin, view some of the existing designs in the list. Clicking on any one will load the style sheet into this very page. The HTML remains the same, the only thing that has changed is the external CSS file. Yes, really.
			4 pCSS allows complete and total control over the style of a hypertext document. The only way this can be illustrated in a way that gets people excited is by demonstrating what it can truly be, once the reins are placed in the hands of those able to create beauty from structure. Designers and coders alike have contributed to the beauty of the web; we can always push it further.

		3 div .participation .zen-participation role[article]
			4 h3 Participation
			4 pStrong visual design has always been our focus. You are modifying this page, so strong CSS skills are necessary too, but the example files are commented well enough that even CSS novices can use them as starting points. Please see the CSS Resource Guide for advanced tutorials and tips on working with CSS.
			4 p You may modify the style sheet in any way you wish, but not the HTML. This may seem daunting at first if you’ve never worked this way before, but follow the listed links to learn more, and use the sample files as a guide.
			4 p Download the sample HTML and CSS to work on a copy locally. Once you have completed your masterpiece (and please, don’t submit half-finished work) upload your CSS file to a web server under your control. Send us a link to an archive of that file and all associated assets, and if we choose to use it we will download it and place it on our server.

		3 div .benefits #zen-benefits role[article]
			4 h3 Benefits
			4 p Why participate? For recognition, inspiration, and a resource we can all refer to showing people how amazing CSS really can be. This site serves as equal parts inspiration for those working on the web today, learning tool for those who will be tomorrow, and gallery of future techniques we can all look forward to.

		3 div .requirements #zen-requirements role[article]
			4 h3 Requirements
			4 p Where possible, we would like to see mostly CSS 1 & 2 usage. CSS 3 & 4 should be limited to widely-supported elements only, or strong fallbacks should be provided. The CSS Zen Garden is about functional, practicalCSS and not the latest bleeding-edge tricks viewable by 2% of the browsing public. The only real requirement we have is that your CSS validates.
			4 p Luckily, designing this way shows how well various browsers have implemented CSS by now. When sticking to the guidelines you should see fairly consistent results across most modern browsers. Due to the sheer number of user agents on the web these days — especially when you factor in mobile — pixel-perfect layouts may not be possible across every platform. That’s okay, but do test in as many as you can. Your design should work in at least IE9+ and the latest Chrome, Firefox, iOS and Android browsers (run by over 90% of the population).
			4 p We ask that you submit original artwork. Please respect copyright laws. Please keep objectionable material to a minimum, and try to incorporate unique and interesting visual themes to your work. We’re well past the point of needing another garden-related design.
			4 p This is a learning exercise as well as a demonstration. You retain full copyright on your graphics (with limited exceptions, see submission guidelines), but we ask you release your CSS under a Creative Commons license identical to the one on this site so that others may learn from your work.

			4 p By 
				5 a Dave Shea. 
			Bandwidth graciously donated by 
				5 a mediatemple. 
			Now available: 
				5 a Zen Garden, the book.

		3 footer
			4 a HTML 
			4 a CSS 
			4 a CC 
			4 a A11y 
			4 a GH

	2 aside .sidebar role[complementary]
		3 div .wrapper
			4 div .design-selection #design-selection
				5 H3 .select Select a Design:
				5 nav role[navigation] 
					6 ul
						7 li
							8 a .design-name Mid Century Modern 
							by 
							8 a .designer-name Andrew Lohman
						7 li
							8 a .design-name Garments 
							by 
							8 a .designer-name Dan Mall
						7 li
							8 a Steel 
							by 
							8 a .designer-name Steffen Knoeller
						7 li
							8 a Apothecary 
							by 
							8 a .designer-name Trent Walton
						7 li
							8 a Screen Filler 	
							by 
							8 a .designer-name Elliot Jay Stocks
						7 li
							8 a Fountain Kiss 
							by 
							8 a .designer-name Jeremy Carlson
						7 li
							8 a A Robot Named Jimmy 
							by 
							8 a .designer-name meltmedia
						7 li
							8 a Verde Moderna 
							by 
							8 a .designer-name Dave Shea

		3 div .design-archives #design-archives
			4 h3 .archives Archives:
			4 nav role[navigation] 
				5 ul
					6 li .next
						a Next Designs ›
					6 li .viwall
						a View All Designs

		3 div .zen-resources #zen-resources
			4 h3 .resources Resources:
			4 ul
				5 li .view-css
					a View This Design’s CSS
				5 li .css-resources
					a
						abbr CSS Resources
				5 li .zen-faq
					a
						abbr FAQ
				5 li .zen-submit
					a Submit a Design
				5 li .view-css
					a Translations

<!-- extra divs for presentation -->
0 div .extra1 role[presentation]
0 div .extra2 role[presentation]
0 div .extra3 role[presentation]
0 div .extra4 role[presentation]
0 div .extra5 role[presentation]
0 div .extra6 role[presentation]
</code>
