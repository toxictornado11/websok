#!/usr/bin/env python3

import asyncio
from websockets.asyncio.client import connect

USER_AGENT = "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/605.1.15 (KHTML, like Gecko) Version/18.6 Safari/605.1.15"

async def hello():
    async with connect("wss://j04.showup.tv/", user_agent_header=USER_AGENT) as websocket:
        await websocket.send('{"id":0,"value":["7774dc65d46d17c0d866e98535acea51",""]}')
        await websocket.send('{"id":2,"value":["_Betty_Barnes"]}')
        print("OK")

        while True:
            message = await websocket.recv()
            print(message)

if __name__ == "__main__":
    asyncio.run(hello())
