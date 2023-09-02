---
title: Subsonic Clients
date: today
author: Me
---
## FOR NOW THIS ONLY A TEST PAGE, DON'T RELY ON IT YET
This will be a list of all Subsonic clients for each device.
[Download yml data ]({{ site.url }}/_data/clients.yml)

<table>
    <tr>
        <th>Client</th>
		<th>Lyrics</th>
		<th>Scrobbling</th>
		<th>Multiple server support</th>
		<th>Offline Music</th>
		<th>Max bitrate setting</th>
		<th>Multiple server</th>
		<th>Free</th>
		<th></th>
		<th></th>
		<th></th>
		<th></th>
    </tr>
	
	{% for c in site.data.clients %}
	
	
    <tr>
		<td>
			<a href = "{{ c.github }}"> 
				{{ c.name }} 
			</a> 
		</td>
		
		<td>
			{% if c.lyrics == true%}
				✔️
			{% elsif c.lyrics == false %}
				❌
			{% else %}
				
			{% endif %}
		</td>
		
		<td>
		</td>
		
		<td>
		</td>
		
		<td>
		</td>
		
		<td>
		</td>
		
		<td>
		</td>
		
		<td>
		</td>
    </tr>
	
	
	
	{% endfor %}
	
</table>

