# Get Location

Using the Google Play services location APIs, your app can request the last known location of the user's device. In most cases, you are interested in the user's current location, which is usually equivalent to the last known location of the device.

# Set up Google Play services

To access the fused location provider, your app's development project must include Google Play services. Download and install the Google Play services component via the SDK Manager and add the library to your project. For details, see the guide to Setting Up Google Play Services.

# Specify app permissions

Apps whose features use location services must request location permissions, depending on the use cases of those features.

# Create location services client

        private FusedLocationProviderClient fusedLocationClient;

        // ..

                @Override
        protected void onCreate(Bundle savedInstanceState) {
           // ...

          fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
        }


        
        
# Get the last known location


        fusedLocationClient.getLastLocation()
        .addOnSuccessListener(this, new OnSuccessListener<Location>() {
            @Override
            public void onSuccess(Location location) {
                // Got last known location. In some rare situations this can be null.
                if (location != null) {
                    // Logic to handle location object
                }
            }
        });


# Choose the best location estimate

**getLastLocation()** gets a location estimate more quickly and minimizes battery usage that can be attributed to your app. However, the location information might be out of date, if no other clients have actively used location recently.

**getCurrentLocation()** gets a fresher, more accurate location more consistently. However, this method can cause active location computation to occur on the device.