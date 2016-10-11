---
layout: page
title: About
permalink: /about
---

```ruby
require 'uri'
class Vienna
  def contact
    "hello@vienna-rb.at"
  end

  def where?
    Struct.new("Location", :name, :address, :details)
    Struct::Location.new("sektor5", "Siebenbrunnengasse 44, 1050 Wien")
  end

  def when?
    Time.new(2014,1,9, 18,00,0, "+01:00")
  end

  def what_and_why?
    URI("http://www.meetup.com/vienna-rb/events/155095492/")
  end

  def who?
    organizers = {
      "Laura Gaetano" => "@alicetragedy",
      "Floor Drees" => "@floordrees",
      "Aaron Cruz" => "@mraaroncruz",
      "Ben Fritsch" => "@beanieboi"}
  end

  def to_s
    where = where?.to_a.compact.join(" ")
   "The next vienna.rb takes place at #{where} and starts at #{when?}. For more see: #{what_and_why?}"
  end


  def version
    "v0.0.4 - 2013-05-30 16:04"
  end
end
```
