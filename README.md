# Asynchronous-
Asynchronous web scraping using Asyncio and Aiohttp.
import aiohttp
import asyncio

async def fetch(url):
    async with aiohttp.ClientSession() as session:
        async with session.get(url) as response:
            return await response.text()

async def main():
    html = await fetch('https://example.com')
    print(html)

asyncio.run(main())
