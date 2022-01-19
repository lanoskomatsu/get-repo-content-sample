generate csv

```ruby
require "csv"

CSV.open("aaa.csv", "wb") do |csv|
  csv << %w(a b c d e f g)
  70000.times do |i|
    csv << [i+1, i+2, i+3, i+4, i+5, i+6, i+7]
  end
end
```

get content

```sh
curl -H "Accept: application/vnd.github.v3.raw" https://api.github.com/repos/lanoskomatsu/get-repo-content-sample/contents/csv/aaa.csv
```