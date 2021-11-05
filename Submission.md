---
layout: default
title: Welcome
---
{% assign Category = '' | split: ',' %}
  {% for recipe in site.recipe %}
    {% for c in recipe.category %}
      {% if Category contains c %}
      {% else %}
      {% assign Category = c | concat: Category %}
      {% endif %}
    {% endfor %}
  {% endfor %}

{% assign Category = Category | sort %}


<div id="general-text">
<h1 style= "text-align: center"> Submission Steps</h1>

<p>
  Currently, the only way to submit is by uploading files to a shared drive folder... If I included direct submission on the site, it would be harder to screen submissions. The Submission folder is synced to the site daily, not instantly.
</p>

<ul>
  <li>Submissions need to be as a .txt or .md file. </li>
  <li>Do not submit a word doc, save file as .txt or .md </li>
  <li> One image is allowed, save image as .jpeg, .jpg, or .png. Be sure that file name matches as written in the text file </li>
  <li> the formatting is very particular, do not add extra spaces. The ingredient and step list can be as long as desired.
  </li> 
  <li> Replace red underlined text with Your Recipe (See Below)</li>
</ul>
</div>

<h4 style= "text-align: center"> Quick Notes</h4>
<div id="general-text">
	<ul>
		<li> Preptime, cooktime, and yield are optional</li>
		<li> At least 1 Category is needed, please choose from list below.</li>
		<ol style="list-style-type: square; padding-bottom: 0;"><li> 
			{% for c in Category %}
			{{c}}, 
			{% endfor %}
		</li></ol>
		<li>  <a style= "color: #00ccff;" href="https://drive.google.com/drive/folders/1XmxNw-vZWsO96-EgeD27eDc0lObsxLF9?usp=sharing"> Drive Link </a> </li><ol style="list-style-type: square; padding-bottom: 0;"> 
			<li>
				access restricted to authorized emails
			</li>
			</ol>
	</ul>
</div>

<h4 style= "text-align: center"> Text File Example</h4>
<pre>

---
layout: recipe

name: <u>10-Minute Lasagna</u>

author: <u>Mary Germick</u>
prep_time: <u>x min</u>
cook_time: <u>x min</u>
yield: <u>x person</u>
Leading_image: <u>IMAGENAME.jpeg</u>
category:
- <u>"Baked"</u>
- <u>"Pasta"</u>
---

## Background 
	<u>
	optional text
	</u>
	
## Ingredients

<u>
- 26 oz jar of Pasta Sauce
- 30 oz bag frozen large Cheese Ravioli
- 10 oz box frozen chopped spinach, thawed & squeezed
- 8 oz shredded Mozzarella Cheese 1/2 cup grated Parmesan Cheese
</u>
## Directions
<u>
1. Coat 9" X 13" pan with cooking spray & spread 1/2 of the sauce on the bottom
2. Arrange 12 ravioli on top & scatter spinach over them
3. Top with half of each cheese
4. Cover with another layer of ravioli and the remaining sauce & cheese
5. Cover with foil & bake @ 350 for 25 minutes
6. Uncover & bake 5-10 minutes more or till bubbly
</u>
</pre>

