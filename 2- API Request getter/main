import requests, json

def get(url):

    response = requests.get(url=url)
    match response.status_code:
        case 200:
            data = response.json()
            with open('output.json', 'w') as f:
                json.dump(data, f, indent=2)
            print("Data gathered. Check output.json")
        case 404:
            print("error 404 : Not found")
        case 403:
            print("error 403 : Access denied")
        case 401:
            print("error 401 : Access denied")
        case 500:
            print("error 500 : Service unavailable")
        case _:
            print("Unknown error")


Running = True
while Running:

    url = input("Enter a url (0 to exit): ")
    if url == "0":
        print("Bye")
        Running = False
    else:
        get(url)