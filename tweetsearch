from twython import Twython, TwythonStreamer

class MyStreamer(TwythonStreamer):

    def init(self):
        self.counter = 0

    def on_success(self, data):
        if 'text' in data:
            self.counter += 1
            if self.counter >= 2:
                print("Ian G. Harris is popular!")


if __name__ == '__main__':

    C_KEY = "XXXXXXXXXXXXXX"
    C_SECRET = "XXXXXXXXXXXXXX"
    A_TOKEN = "XXXXXXXXXXXXXX"
    A_SECRET = "XXXXXXXXXXXXXX"

    stream = MyStreamer(C_KEY, C_SECRET, A_TOKEN, A_SECRET)
    stream.init()
    stream.statuses.filter(track="Ian G. Harris")
