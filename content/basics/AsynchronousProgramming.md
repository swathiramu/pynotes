---
title: Asynchronousprogramming
date: 2026-01-12
author: Your Name
cell_count: 10
score: 10
---

Basic Async Function


```python
import asyncio
async def say_hello():
    print("Hello, World!")
    await asyncio.sleep(1)
    print("Goodbye, World!")
    
await say_hello()

```

    Hello, World!
    Goodbye, World!
    

Running Multiple Tasks Concurrently


```python
import asyncio

async def task1():
    print("Task 1 starting...")
    await asyncio.sleep(2)
    print("Task 1 done!")

async def task2():
    print("Task 2 starting...")
    await asyncio.sleep(1)
    print("Task 2 done!")

async def main():
    await asyncio.gather(task1(), task2())

await main()

```

    Task 1 starting...
    Task 2 starting...
    Task 2 done!
    Task 1 done!
    

Using asyncio.sleep for Delays




```python
import asyncio

async def countdown(n: int):
    while n > 0:
        print(f"Counting down: {n}")
        await asyncio.sleep(1)
        n -= 1
    print("Countdown finished!")
await countdown(5)
```

    Counting down: 5
    Counting down: 4
    Counting down: 3
    Counting down: 2
    Counting down: 1
    Countdown finished!
    

Concurrent HTTP Requests with aiohttp


```python
!pip install aiohttp
```

    Requirement already satisfied: aiohttp in c:\users\swath\.conda\envs\py312\lib\site-packages (3.13.3)
    Requirement already satisfied: aiohappyeyeballs>=2.5.0 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiohttp) (2.6.1)
    Requirement already satisfied: aiosignal>=1.4.0 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiohttp) (1.4.0)
    Requirement already satisfied: attrs>=17.3.0 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiohttp) (25.4.0)
    Requirement already satisfied: frozenlist>=1.1.1 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiohttp) (1.8.0)
    Requirement already satisfied: multidict<7.0,>=4.5 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiohttp) (6.7.0)
    Requirement already satisfied: propcache>=0.2.0 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiohttp) (0.4.1)
    Requirement already satisfied: yarl<2.0,>=1.17.0 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiohttp) (1.22.0)
    Requirement already satisfied: idna>=2.0 in c:\users\swath\.conda\envs\py312\lib\site-packages (from yarl<2.0,>=1.17.0->aiohttp) (3.11)
    Requirement already satisfied: typing-extensions>=4.2 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiosignal>=1.4.0->aiohttp) (4.15.0)
    


```python
import aiohttp
import asyncio

async def fetch_url(session, url):
    async with session.get(url) as response:
        return await response.text()

async def main():
    urls = ["https://example.com", "https://httpbin.org", "https://python.org"]
    async with aiohttp.ClientSession() as session:
        tasks = [fetch_url(session, url) for url in urls]
        results = await asyncio.gather(*tasks)
        for i, content in enumerate(results):
            print(f"Content from URL {i + 1}:\n{content[:100]}...\n")

await main()

```

    Content from URL 1:
    <!doctype html><html lang="en"><head><title>Example Domain</title><meta name="viewport" content="wid...
    
    Content from URL 2:
    <!DOCTYPE html>
    <html lang="en">
    
    <head>
        <meta charset="UTF-8">
        <title>httpbin.org</title>
     ...
    
    Content from URL 3:
    <!doctype html>
    <!--[if lt IE 7]>   <html class="no-js ie6 lt-ie7 lt-ie8 lt-ie9">   <![endif]-->
    <!-...
    
    


```python

```


---
**Score: 10**