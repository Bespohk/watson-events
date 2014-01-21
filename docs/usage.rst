Usage
=====

Using the event dispatcher is a three step process.

1. Create the event dispatcher
2. Add your event listener to the dispatcher
3. Trigger the dispatcher

.. code-block:: python

    from watson.events import dispatcher, types

    dispatcher = dispatcher.EventDispatcher()  # create the dispatcher
    dispatcher.add('MyEvent', lambda x: x.name)  # add your event listener
    result = dispatcher.trigger(types.Event('SampleEvent'))  # trigger the event

    print(result.first())  # 'SampleEvent'
