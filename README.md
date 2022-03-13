## Hello!
I'm NuclearToffee. I'm a free software developer.<br/>
My preferred pronouns are he/him, but any work.

## PGP
Grab my [personal key](personal.gpg), [mail key](mail.gpg), or [both](personal-and-mail.gpg).<br/>
When contacting me, prefer to use my personal key.

## Email
Run the following Python code to find my personal email address.

```python
import hashlib, random

chunks = {
    "aecnlu": "ffb8a12d9bef1e8a1a2ea53ac565d4af227cda7b093ac9670942f9e1ce0bf055",
    "tfrfoe": "8355498d0f03a29db80bd75163c297a73c05255fbce0cd3acd729e2f69c6943f",
    "ote@pr": "d7c735866ee5d5283696f6cea682875e3c7dbd8cb3f0a8470f4b520f96818372",
    "nmloia": "6fee4047a2f26718ec11ce65c769f787928a817a5835bc30e80cb60342d94b42",
    "c.mo": "c8ad4da2dc70350e5843d133eb13d44536616bc76410687ffa8e0590a3754ea1",
}

cache = []
found = []

for x in chunks:
    while True:
        s = "".join(random.sample(x, len(x)))

        if s in cache:
            continue

        if hashlib.sha256(s.encode("utf-8")).hexdigest() == chunks[x]:
            found.append(s)
            break

        cache.append(s)

email = ""
for chunk in found:
    email += chunk

print(email)
```
