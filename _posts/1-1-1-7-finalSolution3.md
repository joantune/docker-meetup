# & A bit beyond
## Compose example

<pre>
    <code data-trim data-noescape>
	version: '2'
services:
  web:
    build: .
    depends_on:
      - db
      - redis
  redis:
    image: redis
  db:
    image: postgres
    
 </code>
</pre>


 
 
 
  
