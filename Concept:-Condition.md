"Condition" is a new concept introduced in RPGItems 3.6. Power won't fire until all of its conditions are met. Each condition has a id. By adding an id to a power's `conditions` property, you add the condition to the power.

If a condition is static, it'll evaluate its result once, before all powers' execution. Else the condition will evaluate its result each time before firing the power that depends on it.

If a condition is critical, it'll abort the trigger if it fails. That is, a non-critical condition prevent powers that depend on it, and a critical condition cancel all the powers after its failure.