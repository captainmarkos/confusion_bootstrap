https://data.austintexas.gov/

Food Establishment Inspection Scores
------------------------------------
Provides food establishment inspection scores performed within the last 3 years. Inspections are conducted in accordance with the Texas Food Establishment Rules (TFER) and City of Austin Codes. Inspections are completed by Environmental Health Officers working for Austin Public Health (APH) Environmental Health Services Division (EHSD).

https://data.austintexas.gov/browse?Additional-Information_Department=Austin+Public+Health&tags=score


curl 'https://data.austintexas.gov/resource/nguv-n54k.json?$where=inspection_date%3E"2017-01-01"&$order=inspection_date&$limit=50000' > 2019.json


https://dev.socrata.com/foundry/data.austintexas.gov/ecmv-9xxi

$.ajax({
    url: "https://data.austintexas.gov/resource/ecmv-9xxi.json",
    type: "GET",
    data: {
      "$limit" : 5000,
      "$$app_token" : "YOURAPPTOKENHERE"
    }
}).done(function(data) {
  alert("Retrieved " + data.length + " records from the dataset!");
  console.log(data);
});
