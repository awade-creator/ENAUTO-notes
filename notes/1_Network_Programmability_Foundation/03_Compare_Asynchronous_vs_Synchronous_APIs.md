# 1.3 Describe the challenges encountered and patterns used when consuming APIs synchronously and asynchronously

## Synchronous

- API calls must wait for the previous call to finish
- Less complex
- Code is less performant with IO bound calls

## Asynchronous

- API calls can be invoked before the previous call has finished
- More complex/difficult to read
- Code is more performant with IO bound calls
- Requires additional `asyncio` library
