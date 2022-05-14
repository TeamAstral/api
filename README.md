<h1 align="center">Astral API</h1>

Before you get started using Astral, there is some basic knowledge you will need to know about. Astral does not require an API Key, which allows for free public access across our entire platform. We adjust our rate limits frequently to match our users needs.
 
### What can this API be used for?
Astral is still very early in development, so the things we offer may change. So far we offer:
- Basic Search
- News Updates
- Hash Cracking

### Database Search

`https://beta.database.report/api/search/{target}/{type}`


Send a query request and output all breaches for `target` into a format of `type`

___________________

| Target | Accepted |
| :-: | :-: |
| str (email, hash, password, ip address) | ✔ |
| uuid (base, minecraft) | ✔ |
| int (epoch, plain integer) | ❌ |
| bool | ❌ |

| Type | Resp |
| :-: | :-: |
| json | output into a prettify'd JSON list |
| plain | get a plaintext output |
| none | defaults to json outputs |

___________________

EX: `GET https://beta.database.report/api/search/magicmanlogan@gmail.com/json`
## RESP
```json
{
  "response": "success",
  "results": [
    {
      "minecraft_hacked_logins": "magicmanlogan@gmail.com:loganrocks - Rogen"
    },
    {
      "ogusers.com_dehashed": "magicmanlogan@gmail.com:loganrocks"
    }
  ]
}
```
