    <li>
      <h2><a href="{{ recipe.url }}">{{ recipe.name }}</a></h2>
      <p>{{ recipe.cook_time | markdownify }} {{ recipe.prep_time | markdownify }} </p>
    </li>


Quick commands

run on command line to replace files with baked in current directory to Baked

grep -rl 'baked' . |xargs sed -i 's/baked/Baked/g'

list files with matching string

grep -IRl Marinated/spice *
