# Testing

I was testing the functionality of the `SelectWord` function of the game. Unfortunately the function was private and tied within the `ContentPage` MAUI class making unit testing difficult, thus the examples I have given are more theoretical as we couldn't get the tests working. The function in question selects the word for the game depending on a difficulty string input. While the contents of this string will not come directly from a user, it is still good to check the functionality when an invalid input is given. In a real world project this would be vital testing, as not correctly handling this can lead to a cascading failure.

```C#
[Fact]
public void EmptyStringInput() {
    Assert.ThrowsAsync<Exception>(() => new GamePage(""));
}

[Fact]
public void InvalidStringInput() {
    Assert.ThrowsAsync<Exception>(() => new GamePage("INVALID GAME TYPE STRING"));
}
```

We test both an empty string and an invalid string. We assume that this must throw an exception that will be caught and handled somewhere outside of the word selection abstraction.