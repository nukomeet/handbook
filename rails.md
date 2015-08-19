# Common validations for Rails


## for `User`

```
validates :email, :username,  presence: true, uniqueness: { case_sensitive: false }
validates :username, format: { with: /\A\w+\Z/i }, length: { in: 2..12 }, presence: true, uniqueness: true
```

## for `Address`

```
validates :name, length: { in: 5..45 }                              
validates :desc, length: { in: 5..500 }, presence: true             
validates :address_line1, presence: true
validates :city, presence: true, format: { with: /\A[a-zA-Z]+[\s\D]+[a-zA-Z]+\z/i }
validates :country, presence: true
```