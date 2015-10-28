---
layout: post
title:  Coursework
date:   2015-10-08
categories: notes
permalink: /coursework/
---

Advisor - Mitchell Joachim (now Meleko Mokgosi)

### Spring 2013

- Art: Practice and Ideas - Artie Vierkant
- Evolution of Intellectual Complexity - Ray Dougherty
- Origin of Humanity - Stephanos Geroulanos
- Think Big: Global Issues and Ecological Solutions - Mitchell Joachim

### Fall 2012

- Art in Critical Theory - Meleko Mokgosi
- Computers and Society - Evan Korth
- Creative Fundraising - Wilder Knight/Ed DePalma
- Interdisciplinary Undergraduate Projects in Studio Art: Sex and Contemporary Art - Kathe Burkhart

### Spring 2012

- Art of Now - Haley Mellin
- Intro to Physical Computing - Scott Fitzgerald
- Rise of Internet Media - Aaron Cohen
- Urban Desires: Sex, Gender and New York City - Neil Meyer

### Fall 2011
- Artists' Lives, Artists' Work - Yevgeniya Traps
- Family - Patrick McCreery
- Intro to Painting I - Kevin Yang
- Social Entrepreneurship - Andrew Greenblatt

{% raw %}
<script>
var coursework = {
	"data": {
		"allSemesters": ["spring13", "fall12", "spring12", "fall11"],
		"allRankings": [
			{
				"rankGrade": "A",
				"rankDescription": "excellent"
			},
			{
				"rankGrade": "B",
				"rankDescription": "satisfactory"
			},
			{
				"rankGrade": "C",
				"rankDescription": "I was not ready"
			},
			{
				"rankGrade": "D",
				"rankDescription": "not for me"
			}
		],
		"spring13": {
			"courses": [
				{
					"title": "Art in Critical Theory",
					"objective": {
						"professor": "Meleko Mokgosi",
						"tags": ["art", "theory", "political economy", "psychoanalysis"]
					},
					"subjective": {
						
					}
				}
			]
		},
		"fall12": {

		},
		"spring12": {

		},
		"fall11": {

		}
	},
	"init": function() {
		console.log(coursework);
		console.log("think you're happy now!")
	}
}


$(document).ready( function() {
	coursework.init();
});

</script>

{% endraw %}