---
title: Asynchronous Programming
date: 2026-01-09
author: Your Name
cell_count: 11
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
    


```python
!pip install aiohttp
```

    Collecting aiohttp
      Using cached aiohttp-3.13.3-cp312-cp312-win_amd64.whl.metadata (8.4 kB)
    Collecting aiohappyeyeballs>=2.5.0 (from aiohttp)
      Using cached aiohappyeyeballs-2.6.1-py3-none-any.whl.metadata (5.9 kB)
    Collecting aiosignal>=1.4.0 (from aiohttp)
      Using cached aiosignal-1.4.0-py3-none-any.whl.metadata (3.7 kB)
    Requirement already satisfied: attrs>=17.3.0 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiohttp) (25.4.0)
    Collecting frozenlist>=1.1.1 (from aiohttp)
      Using cached frozenlist-1.8.0-cp312-cp312-win_amd64.whl.metadata (21 kB)
    Collecting multidict<7.0,>=4.5 (from aiohttp)
      Using cached multidict-6.7.0-cp312-cp312-win_amd64.whl.metadata (5.5 kB)
    Collecting propcache>=0.2.0 (from aiohttp)
      Using cached propcache-0.4.1-cp312-cp312-win_amd64.whl.metadata (14 kB)
    Collecting yarl<2.0,>=1.17.0 (from aiohttp)
      Using cached yarl-1.22.0-cp312-cp312-win_amd64.whl.metadata (77 kB)
    Requirement already satisfied: idna>=2.0 in c:\users\swath\.conda\envs\py312\lib\site-packages (from yarl<2.0,>=1.17.0->aiohttp) (3.11)
    Requirement already satisfied: typing-extensions>=4.2 in c:\users\swath\.conda\envs\py312\lib\site-packages (from aiosignal>=1.4.0->aiohttp) (4.15.0)
    Using cached aiohttp-3.13.3-cp312-cp312-win_amd64.whl (455 kB)
    Using cached multidict-6.7.0-cp312-cp312-win_amd64.whl (46 kB)
    Using cached yarl-1.22.0-cp312-cp312-win_amd64.whl (87 kB)
    Using cached aiohappyeyeballs-2.6.1-py3-none-any.whl (15 kB)
    Using cached aiosignal-1.4.0-py3-none-any.whl (7.5 kB)
    Using cached frozenlist-1.8.0-cp312-cp312-win_amd64.whl (44 kB)
    Using cached propcache-0.4.1-cp312-cp312-win_amd64.whl (41 kB)
    Installing collected packages: propcache, multidict, frozenlist, aiohappyeyeballs, yarl, aiosignal, aiohttp
    
       ---------------------------------------- 0/7 [propcache]
       ----- ---------------------------------- 1/7 [multidict]
       ----------------- ---------------------- 3/7 [aiohappyeyeballs]
       ---------------------- ----------------- 4/7 [yarl]
       ---------------------- ----------------- 4/7 [yarl]
       ---------------------- ----------------- 4/7 [yarl]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------- ----- 6/7 [aiohttp]
       ---------------------------------------- 7/7 [aiohttp]
    
    Successfully installed aiohappyeyeballs-2.6.1 aiohttp-3.13.3 aiosignal-1.4.0 frozenlist-1.8.0 multidict-6.7.0 propcache-0.4.1 yarl-1.22.0
    

Concurrent HTTP Requests with aiohttp


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

a
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
    
    

Producer-Consumer Pattern


```python
import asyncio

async def producer(queue):
    """Produces numbers 0-4 and puts them into the queue"""
    for i in range(5):
        print(f"Producing {i}")
        await queue.put(i) 
        await asyncio.sleep(1)
    print("Producer done producing.")

async def consumer(queue):
    """Consumes items from the queue until queue is empty"""
    while True:
        item = await queue.get() 
        print(f"Consuming {item}")
        queue.task_done() 
        if queue.empty():
            break
    print("Consumer done consuming.")

async def main():
    queue = asyncio.Queue()
    producer_task = asyncio.create_task(producer(queue))
    await asyncio.sleep(0.1)
    consumer_task = asyncio.create_task(consumer(queue))
    await producer_task
    await queue.join()
    if not consumer_task.done():
        consumer_task.cancel()
    print("All tasks completed!")

await main()

```

    Producing 0
    Consuming 0
    Consumer done consuming.
    Producing 1
    Producing 2
    Producing 3
    Producing 4
    Producer done producing.
    


---
**Score: 10**