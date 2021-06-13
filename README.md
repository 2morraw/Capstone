# Capstone
Coursera Capstone Project 

toronto = folium.Map(location = [latitude, longitude], zoom_start = 10)

for lat,lng,borough,neighbourhood in zip(df_2['Latitude'],df_2['Longitude'],df_2['Borough'],df_2['Neighborhood']):
    label = '{}, {}'.format(neighbourhood, borough)
    label = folium.Popup(label, parse_html = True)
    folium.CircleMarker(
    [lat, lng],
    radius = 5,
    popup = label,
    color = 'black',
    fill = True,
    fill_color = 'yellow',
    fill_opacity = 0.7,
    parse_html = False).add_to(toronto)
    
toronto
