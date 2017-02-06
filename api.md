## API DOC

### Endpoints

1. GET `/api/v1/organizations`

*Response*

```JSON
{
  "data": [
    {
      "id": 1,
      "name": "GCT Labs",
      "description": "GCT Labs is the software development division of the Congress WBN GCT Sector",
      "slug": "gctlabs",
      "logo": "http://sensa.dev/img/tenant_logo_placeholder.png",
      "header_logo": "http://sensa.dev/img/tenant_logo_placeholder.png",
      "tenantFooter": {
        "data": {
          "id": 5,
          "key": "tenant-footer-html",
          "value": "<p>Hello</p>"
        }
      }
    },
    {
      "id": 2,
      "name": "authLab",
      "description": "authLab is a team of designers, developers, software architects and tech enthusiasts aimed to craft and develop your web entity.",
      "slug": "authlab",
      "logo": "http://sensa.dev/img/tenant_logo_placeholder.png",
      "header_logo": "http://sensa.dev/img/tenant_logo_placeholder.png"
    }
  ]
}
```

**Includes**
------------
`tenantHeader`

```$xslt
"tenantHeader": {
    "data": {
      "id": 4,
      "key": "tenant-header-colors",
      "value": "{\"primary\":\"#73422\",\"secondary\":\"#73422\"}"
    }
  }
```
2. GET `/api/v1/organizations/{tenantSlug}/regions`

*Response*

```
{
  "data": [
    {
      "id": 1,
      "name": "Asia",
      "slug": "asia",
      "description": "",
      "country_count": 2,
      "entity_count": 1
    },
    {
      "id": 3,
      "name": "Africas",
      "slug": "africas",
      "description": "Woo ",
      "country_count": 1,
      "entity_count": 1
    }
  ]
}
```

### Includes
`leaderships`

*Response*

```$javascript
"leaderships": {
    "data": [
      {
        "id": 1,
        "user": {
          "data": {
            "id": 26,
            "sensa_id": null,
            "username": "frankramnanan",
            "email": "frank.ramnanan@congressmail.com",
            "name": "Frank  Ramnanan",
            "first_name": "Frank",
            "middle_name": null,
            "last_name": "Ramnanan",
            "gender": null,
            "date_of_birth": null,
            "place_of_birth": null,
            "blood_type": null,
            "profile_photo_small": "http://sensa.dev/img/default_profile_pic.jpg",
            "profile_photo_large": "http://sensa.dev/img/default_profile_pic.jpg",
            "bio": null,
            "role": null,
            "is_verified": true
          }
        }
      }
    ]
}
```

`leaderships.type`

*Response*

```$javascript
"type": {
  "data": {
    "id": 1,
    "title": "Co-Ordinator"
  }
}
```

### Default Includes

`leaderships.user`

*Response*

```$javascript
"user": {
  "data": {
    "id": 26,
    "sensa_id": null,
    "username": "frankramnanan",
    "email": "frank.ramnanan@congressmail.com",
    "name": "Frank  Ramnanan",
    "first_name": "Frank",
    "middle_name": null,
    "last_name": "Ramnanan",
    "gender": null,
    "date_of_birth": null,
    "place_of_birth": null,
    "blood_type": null,
    "profile_photo_small": "http://sensa.dev/img/default_profile_pic.jpg",
    "profile_photo_large": "http://sensa.dev/img/default_profile_pic.jpg",
    "bio": null,
    "role": null,
    "is_verified": true
  }
}
```

`countries`

*Response*

```$javascript
"countries": {
"data": [
  {
    "id": 195,
    "name": "South Africa",
    "entities": {
      "data": [
        {
          "id": 13,
          "parent_id": "12",
          "tenant_id": "5",
          "slug": "ec-embassy-miami",
          "name": "Elijah Centre Embassy Miami",
          "tag_line": null,
          "website": "http://www.elijahcentre.org",
          "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
          "featured_image": null
        }
      ]
    }
  }
]
}
```


3. GET `api/v1/organizations/{tenantSlug}/regions/{regionId}`

*Response*

```$javascript
{
  "data": {
    "id": 1,
    "name": "Asia",
    "slug": "asia",
    "description": "",
    "country_count": 2,
    "entity_count": 1
  }
}
```

4. GET `/api/v1/organizations/{tenantSlug}/countries`

*Response*

```$javascript
{
  "data": [
    {
      "id": 18,
      "name": "Bangladesh",
      "entities": {
        "data": [
          {
            "id": 11,
            "parent_id": "0",
            "tenant_id": "5",
            "slug": "ec-nexus",
            "name": "Elijah Centre Nexus",
            "tag_line": null,
            "website": "http://www.elijahcentre.org",
            "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
            "featured_image": null,
            "entityType": {
              "data": {
                "id": 9,
                "name": "Community"
              }
            }
          }
        ]
      }
    }
    ...
  ]
}
```

### Default Include

`entities`

*Response*

```$javascript
"entities": {
    "data": [
      {
        "id": 11,
        "parent_id": "0",
        "tenant_id": "5",
        "slug": "ec-nexus",
        "name": "Elijah Centre Nexus",
        "tag_line": null,
        "website": "http://www.elijahcentre.org",
        "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
        "featured_image": null,
        "entityType": {
          "data": {
            "id": 9,
            "name": "Community"
          }
        }
      }
    ]
}
```

5. GET `/api/v1/organizations/{tenantSlug}/countries/{countryId}`

*Response*

```$javascript
{
  "data": {
    "id": 18,
    "name": "Bangladesh",
    "entities": {
      "data": [
        {
          "id": 11,
          "parent_id": "0",
          "tenant_id": "5",
          "slug": "ec-nexus",
          "name": "Elijah Centre Nexus",
          "tag_line": null,
          "website": "http://www.elijahcentre.org",
          "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
          "featured_image": null,
          "entityType": {
            "data": {
              "id": 9,
              "name": "Community"
            }
          }
        }
      ]
    }
  }
}
```

6. GET `/api/v1/organizations/{tenantSlug}/entities`

*Response*

```$javascript
{
  "data": [
    {
      "id": 11,
      "parent_id": "0",
      "tenant_id": "5",
      "slug": "ec-nexus",
      "name": "Elijah Centre Nexus",
      "tag_line": null,
      "website": "http://www.elijahcentre.org",
      "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
      "featured_image": null
    },
    {
      "id": 12,
      "parent_id": "0",
      "tenant_id": "5",
      "slug": "ec-embassies",
      "name": "Elijah Centre Embassies",
      "tag_line": null,
      "website": null,
      "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
      "featured_image": null
    },
    ...
]
```

### Available Include

`entityType`

*Response*

```$javascript
"entityType": {
    "data": {
      "id": 9,
      "name": "Community"
    }
}
```

`addresses`

*Response*

```$javascript
"addresses": {
    "data": [
      {
        "id": 1,
        "address_line_1": "Address line 11",
        "address_line_2": "Road 3323",
        "city": "Sylhet",
        "state": "Sylhet",
        "postal_code": "3100"
      },
      {
        "id": 2,
        "address_line_1": "Adress 2",
        "address_line_2": "Road 83474832",
        "city": "Sylget",
        "state": "Siuwey",
        "postal_code": "w4234"
      }
    ]
  }
```

`addresses.contactType`

*Response*

```$javascript
"contactType": {
  "data": {
    "id": 7,
    "name": "Work",
    "resource_type": "contact_addresses"
  }
}
```

`addresses.country`

*Response*

```$javascript
"country": {
  "data": {
    "id": 18,
    "name": "Bangladesh"
  }
}
```

`phones`

*Response*

```$javascript
"phones": {
    "data": [
      {
        "id": 1,
        "number": "7435873468576"
      },
      {
        "id": 2,
        "number": "7456437658365834"
      }
    ]
}
```

`phones.contactType`

*Response*

```$javascript
"contactType": {
  "data": {
    "id": 14,
    "name": "Home",
    "resource_type": "contact_phones"
  }
}
```

`emails`

*Response*

```$javascript
"emails": {
    "data": [
      {
        "id": 1,
        "email": "anwar@google.it"
      },
      {
        "id": 2,
        "email": "down-arrow@jdhhjuslf.com"
      }
    ]
}
```

`emails.contactType`

*Response*

```$javascript
"contactType": {
  "data": {
    "id": 2,
    "name": "Personal",
    "resource_type": "contact_emails"
  }
}
```

`leaderships`

*Response*

```$javascript
"leaderships": {
    "data": [
      {
        "id": 1
      },
      {
        "id": 2
      }
    ]
}
```

`leaderships.type`

*Response*

```$javascript
"type": {
  "data": {
    "id": 2,
    "title": "Manager"
  }
}
```

`leaderships.user`

*Response*

```$javascript
"user": {
  "data": {
    "id": 26,
    "sensa_id": null,
    "username": "frankramnanan",
    "email": "frank.ramnanan@congressmail.com",
    "name": "Frank  Ramnanan",
    "first_name": "Frank",
    "middle_name": null,
    "last_name": "Ramnanan",
    "gender": null,
    "date_of_birth": null,
    "place_of_birth": null,
    "blood_type": null,
    "profile_photo_small": "http://sensa.dev/img/default_profile_pic.jpg",
    "profile_photo_large": "http://sensa.dev/img/default_profile_pic.jpg",
    "bio": null,
    "role": null,
    "is_verified": true
  }
}
```

7. GET `/api/v1/organizations/{tenantSlug}/entities/{entitySlug}`

*Response*

```$javascript
{
  "data": {
    "id": 11,
    "parent_id": "0",
    "tenant_id": "5",
    "slug": "ec-nexus",
    "name": "Elijah Centre Nexus",
    "tag_line": null,
    "website": "http://www.elijahcentre.org",
    "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
    "featured_image": null
  }
}
```

7. GET `/api/v1/organizations/{tenantSlug}/entities?search={searchString}`

*Response*

```angular2html
{
  "data": [
    {
      "id": 11,
      "parent_id": "0",
      "tenant_id": "5",
      "slug": "ec-nexus",
      "name": "Elijah Centre Nexus",
      "tag_line": null,
      "website": "http://www.elijahcentre.org",
      "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
      "featured_image": null
    },
    {
      "id": 12,
      "parent_id": "0",
      "tenant_id": "5",
      "slug": "ec-embassies",
      "name": "Elijah Centre Embassies",
      "tag_line": null,
      "website": null,
      "logo": "http://sensa.dev/img/entity_logo_placeholder.png",
      "featured_image": null
    },
    ...
  ]
}
```
