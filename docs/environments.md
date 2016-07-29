# Environment Variables

Insomnia supports the ability to share common settings across requests so that you can manage them
in one place. The environment is defined as JSON, so you can put whatever you want in it. 

**Sample Environment:**

```
{
	"base_url": "https://api.myproduct.com/v1",
	"api_key": "live_0a7b973038f4f6ee5",
	"user_id": "user_0138tsrat8902n4pt",
	"name": "gregory schier",
	"locales": {
		"english": "en-US",
		"french": "fr-FR"
	}
}
```

You can reference the environment in any request by using the
[Nunjucks](https://mozilla.github.io/nunjucks/) template syntax.


**Sample URL:**

```twig
{{ base_url }}/users/{{ user_id }}
```


**Sample JSON Request body:**

```twig
{
  "type": "User",
  "id": "{{ user_id }}",
  "name": "{{ name | title }}",
  "locale": "{{ locales.english }}"
}
```
