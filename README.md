# Indonesian Postal and Geolocation Data

## Initial Data Source
1. ArrayAccess

    Project created to make postalcode autocomplete feature. I just use this data to collect the geocode location point. Please look at the [documentation](https://www.arrayiterator.com/kodepos-geocoding-json-seluruh-indonesia-sesuai-bps) and [github repo](https://github.com/ArrayAccess/Indonesia-Postal-And-Area)

2. Badan Pusat Statistik
    
    Used as an initial data on this project. Please look at the [website](https://sig.bps.go.id/bridging-kode/index) 

3. KodePosku 

    A single csv file that contain postalcode, province, district, regency, and kode_kemendagri. Please look at the [documentation](https://kodeposku.com/dokumentasi)

4. Coll-J 

    Approximating the latitude and longitude using the mean of borders. Using single csv as a initial data and create separated csv group by province, district, and regency that have general geocode location. Please look at the [github repo](https://github.com/coll-j/indonesia-locations-data)


## Order
1. Run `main.ipynb` to get the latest pair of administratif location of Indonesian from **Badan Pusat Statistik**
2. Run `geocode-base-aa.ipynb` to get the geolocation point of every administratif location of Indonesian. In short, I only left join the [BPS](https://sig.bps.go.id/bridging-kode/index) data and data from [ArrayAccess](https://github.com/ArrayAccess/Indonesia-Postal-And-Area)
3. Because there're several data that still have unknown point of location. We use data from [coll-j](https://github.com/coll-j/indonesia-locations-data) to fill the missing value. especially for regency locations data. Look at the `geocode-base-coll.ipynb` file
4. Another data that i collect are postal code. Look at the `postal-code.ipynb`
5. `final.ipynb` created just to choose each final files from the output folders and put it on final folders.


# Disclaimer
I don't know the validity of the existing initial data except data from Badan Pusat Statistik (BPS), but let's just say that the existing initial data is quite accurate. I also can't guarantee the coordinates are 100% correct.