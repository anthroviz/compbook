---
layout: post
title:  Coursework
date:   2015-10-08
categories: notes
permalink: /coursework/
---

{% raw %}
<div class="coursework__ranks">
	
</div>
{% endraw %}

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
		"allRankings": ["A", "B", "C", "D"],
		"ranks": {
			"A": {
				"rankDescription": "excellent"
			},
			"B": {
				"rankDescription": "satisfactory"
			},
			"C" : {
				"rankDescription": "I was not ready"
			},
			"D": {
				"rankDescription": "not for me"
			}
		},
		"spring13": {
			"fullName": "Spring 2013",
			"courses": [
				{
					"title": "Art: Practice and Ideas",
					"objective": {
						"professor": "Artie Vierkant",
						"tags": ["art", "theory", "contemporary-art"]
					},
					"subjective": {
						"rank": "A"
					}
				},
				{
					"title": "Evolution of Intellectual Complexity",
					"objective": {
						"professor": "Ray Dougherty",
						"tags": ["linguistics", "biology", "origins"]
					},
					"subjective": {
						"rank": "A"
					}
				}
			]
		},
		"fall12": {
			"fullName": "Fall 2012",
			"courses": [
				{
					"title": "Art in Critical Theory",
					"objective": {
						"professor": "Meleko Mokgosi",
						"tags": ["art", "theory", "political-economy", "psychoanalysis"]
					},
					"subjective": {
						"rank": "A"
					}
				}
			]
		},
		"spring12": {
			"fullName": "Spring 2012",
			"courses": [

			]
		},
		"fall11": {
			"fullName": "Fall 2011",
			"courses": []
		}
	},
	"reading": function(dataset) {
		var flatArray = [];
		for (var i = 0; i < dataset.length; i++) {
			var currentFlag = dataset[i];

			flatArray.push(coursework.data[currentFlag]);
		}
		return flatArray;
	},
	"assembleCourses": function() {
		var htmlTemplate = [];
		var readSemesters = coursework.reading(coursework.data.allSemesters);

		for (var j = 0; j < readSemesters.length; j++) {
			var thisSemester = readSemesters[j];

			htmlTemplate.push('<div class="semester">' + '<h1>' + thisSemester.fullName + '</h1>');
			if (!!thisSemester.courses) {
				// COURSES
				for (var k = 0; k < thisSemester.courses.length; k++) {
					var thisCourse = thisSemester.courses[k];
					htmlTemplate.push('<div class="semester__course">' + "<h1>" + thisCourse.title + "</h1>" + "<h5>" + thisCourse.objective.professor + "</h5>" + '</div>');
				}
			}
			htmlTemplate.push('</div>');
		}
		return htmlTemplate.join("");
	},
	"init": function() {
		console.log(coursework);
		console.log("think you're happy now!");

		$(".coursework__ranks").append(coursework.assembleCourses());
	}
}


$(document).ready( function() {
	coursework.init();
});
</script>

<style>
.coursework__ranks {
	border: 1px solid black;
	box-sizing: border-box;
	margin: 0;
	padding: 0;
}
.semester, .semester__course {
	border: 1px solid #aaa;
	padding: 1em;
}
.semester__course {
	width: 40%;
	display: inline-block;
}
</style>
{% endraw %}