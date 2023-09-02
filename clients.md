---
title: Subsonic Clients
date: today
author: Me
---
[Download raw yml data ](https://github.com/ArtiskOnGit/subsonic_clients/blob/main/_data/clients.yml)


{% assign platforms = "android, iOS, mac, windows, linux, web" | split: ", " %}

THIS IS A WIP, FEEL FREE TO HELP

# ALL CLIENTS
<table>
	<tr>
		{% for e in site.data.entries %}
			{%if e.show == true%}
			<th>{{ e.name }}	</th>
			{% endif %}
		{% endfor %}
	
	</tr>
	{% for c in site.data.clients %}
	 
	<tr>
		{% for e in site.data.entries %}
			{%if e.show == true%}
				 <td>
					{%if e.type == 'string'%}
						{{ c[e.name] }}
						
					{% elsif  e.type == 'link'%}
						<a href = "{{c[e.name][1]}}"> 
							{{c[e.name][0]}} 
						</a>
						
					{% elsif  e.type == 'bool'%}
						{% if c[e.name]%}
							✔️
						{% elsif c[e.name] == false %}
							❌
						{% else %}
					a
						{% endif %}
					{% else %}
					?
					
					{% endif %}
				</td>
			{% endif %}
			
		{% endfor %}
	</tr>
	{% endfor %}
	
</table>

{% for p in platforms %}

## {{p | upcase}} CLIENTS
<table>
	<tr>
		{% for e in site.data.entries %}
			{%if e.show == true%}
			<th>{{ e.name }}	</th>
			{% endif %}
		{% endfor %}
	
	</tr>
	{% for c in site.data.clients %}
	 {% if c.Platform contains p %}
	<tr>
		{% for e in site.data.entries %}
			{%if e.show == true%}
				 <td>
					{%if e.type == 'string'%}
						{{ c[e.name] }}
						
					{% elsif  e.type == 'link'%}
						<a href = "{{c[e.name][1]}}"> 
							{{c[e.name][0]}} 
						</a>
						
					{% elsif  e.type == 'bool'%}
						{% if c[e.name]%}
							✔️
						{% elsif c[e.name] == false %}
							❌
						{% else %}
					a
						{% endif %}
					{% else %}
					?
					
					{% endif %}
				</td>
			{% endif %}
			
		{% endfor %}
	</tr>
	{% endif %}
	{% endfor %}
	
</table>


{% endfor %}
