# Queue

A simple FIFO (First In, First Out) Queue collection for Zen with type-specific operations for:

- `int`
- `bool`
- `double`
- `long`
- `byte`
- `string`

## Installation

    zen install queue

## Usage

    import (Queue) from "queue"

    Queue q

    q.enqueueInt(10)
    q.enqueueInt(20)
    q.enqueueInt(30)

    screen(q.peekInt())     // 10
    screen(q.dequeueInt())  // 10
    screen(q.dequeueInt())  // 20

## API

### Integer

    q.enqueueInt(value)
    q.dequeueInt()
    q.peekInt()
    q.sizeInt()
    q.isEmptyInt()

### Boolean

    q.enqueueBool(value)
    q.dequeueBool()
    q.peekBool()
    q.sizeBool()
    q.isEmptyBool()

### Double

    q.enqueueDouble(value)
    q.dequeueDouble()
    q.peekDouble()
    q.sizeDouble()
    q.isEmptyDouble()

### Long

    q.enqueueLong(value)
    q.dequeueLong()
    q.peekLong()
    q.sizeLong()
    q.isEmptyLong()

### Byte

    q.enqueueByte(value)
    q.dequeueByte()
    q.peekByte()
    q.sizeByte()
    q.isEmptyByte()

### String

    q.enqueueString(value)
    q.dequeueString()
    q.peekString()
    q.sizeString()
    q.isEmptyString()

## Behavior

Queue follows FIFO ordering:

    q.enqueueInt(10)
    q.enqueueInt(20)
    q.enqueueInt(30)

    q.dequeueInt() // 10
    q.dequeueInt() // 20
    q.dequeueInt() // 30

`enqueue*()` adds a value to the back of the queue.

`dequeue*()` returns and removes the value at the front of the queue.

`peek*()` returns the value at the front without removing it.

`size*()` returns the number of values currently stored for that type.

`isEmpty*()` returns `true` when the corresponding queue is empty.

## Supported Types

| Type | Enqueue | Dequeue | Peek | Size | Is Empty |
|------|---------|---------|------|------|----------|
| `int` | `enqueueInt()` | `dequeueInt()` | `peekInt()` | `sizeInt()` | `isEmptyInt()` |
| `bool` | `enqueueBool()` | `dequeueBool()` | `peekBool()` | `sizeBool()` | `isEmptyBool()` |
| `double` | `enqueueDouble()` | `dequeueDouble()` | `peekDouble()` | `sizeDouble()` | `isEmptyDouble()` |
| `long` | `enqueueLong()` | `dequeueLong()` | `peekLong()` | `sizeLong()` | `isEmptyLong()` |
| `byte` | `enqueueByte()` | `dequeueByte()` | `peekByte()` | `sizeByte()` | `isEmptyByte()` |
| `string` | `enqueueString()` | `dequeueString()` | `peekString()` | `sizeString()` | `isEmptyString()` |

## License

MIT
