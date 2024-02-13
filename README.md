# InternetSpeedtest

https://www.speedtest.net/api/js/servers?engine=js&https_functional=true&limit=100&search=Germany

    {
        "url": "http://dus.wsqm.telekom-dienste.de:8080/speedtest/upload.php",
        "lat": "51.2256",
        "lon": "6.7828",
        "distance": 40,
        "name": "Dusseldorf",
        "country": "Germany",
        "cc": "DE",
        "sponsor": "Deutsche Telekom",
        "id": "30906",
        "preferred": 0,
        "https_functional": 1,
        "host": "dus.wsqm.telekom-dienste.de.prod.hosts.ooklaserver.net:8080",
        "force_ping_select": 1
    }


import speedtest

st = speedtest.Speedtest(secure=True) 

while True:  
    download_speed = st.download()  
    print('Download Speed: {:5.2f} Mb'.format(download_speed/(1024*1024) ))


####

import speedtest

# Server der Telekom in Frankfurt
server_host = "speedtest-frankfurt.telekom.de"

# Speedtest durchführen
speedtest_results = speedtest.Speedtest().get_speed(server_host)

# Ergebnisse ausgeben
print("Download-Geschwindigkeit:", speedtest_results["download"])
print("Upload-Geschwindigkeit:", speedtest_results["upload"])
print("Ping:", speedtest_results["ping"])


