# laravel-tdd README

This is the README for your extension "laravel-tdd". After writing up a brief description, we recommend including the following sections.

## [Todo](http://otroblogmas.com/wp-content/uploads/2011/06/PHPUnit-Cheat-Sheet.pdf)

- [ ] Test all if working
- [x] Laravel TDD HTTP
- [x] Laravel TDD Database
- [x] Laravel TDD Auth
- [x] Laravel TDD Console
- [x] Laravel TDD Verb Actions
- [ ] Laravel TDD API Calls
- [ ] PHPUnit Basic
- [ ] PHPUnit String
- [ ] PHPUnit XML and HTML
- [ ] PHPUnit Fixtures (SetUP and Teardown)
- [ ] PHPUnit Files
- [ ] PHPUnit Array
- [ ] PHPUnit Object
- [ ] PHPUnit CLass Object

* factory define as merge with User main factory

```php
$factory->defineAs(App\User::class, 'admin', function ($faker) use ($factory) {
    $user = $factory->raw(App\User::class);

    return array_merge($user, ['admin' => true]);
});
```

- deprecated http assertion

```php
// assertResponseOk
->assertResponseOk();
// Assert that the client response has an OK status code.
// assertResponseStatus
->assertResponseStatus($code);
// Assert that the client response has a given code.
// assertRedirectedTo
->assertRedirectedTo($uri, $with = []);
// Assert whether the client was redirected to a given URI.
// assertHasOldInput
->assertHasOldInput();
// Assert that the session has old input.
// assertRedirectedToAction
->assertRedirectedToAction($name, $parameters = [], $with = []);
// Assert whether the client was redirected to a given action.
// assertRedirectedToRoute
->assertRedirectedToRoute($name, $parameters = [], $with = []);
// Assert whether the client was redirected to a given route.

// seeJson
->seeJson(array $data)
// seeJsonEquals
->seeJsonEquals(array $data)
// seeJsonStructure
->seeJsonStructure(array $data)
// caa
->call($verb,$uri,$data)
```

- deprecated database assertion

```php
// seeInDatabase
$this->seeInDatabase('users', ['email' => 'sally@example.com']);
```

- acting as using passport

```php
Passport::actingAs(
        factory(User::class)->create(),
        ['create-servers']
    );
```

- make an incomplete test

```php
markTestIncomplete(string $message) - shows I on result
markTestSkipped(string $message) - shows S on result
```

- read more on assertion on phpunit on this [Documentation](https://phpunit.readthedocs.io/en/7.4/assertions.html)

[Example SNippets Click Here](https://github.com/onecentlin/phpunit-snippets-vscode/blob/master/snippets/snippets.json)

- filter test

```php
phpunit --filter define_method_name
```

- Only test Units

```php
phpunit tests/Unit
```

- Only test Feature

```php
phpunit tests/Feature
```

## Features

Describe specific features of your extension including screenshots of your extension in action. Image paths are relative to this README file.

For example if there is an image subfolder under your extension project workspace:

\!\[feature X\]\(images/feature-x.png\)

> Tip: Many popular extensions utilize animations. This is an excellent way to show off your extension! We recommend short, focused animations that are easy to follow.

## Requirements

If you have any requirements or dependencies, add a section describing those and how to install and configure them.

## Extension Settings

Include if your extension adds any VS Code settings through the `contributes.configuration` extension point.

For example:

This extension contributes the following settings:

- `myExtension.enable`: enable/disable this extension
- `myExtension.thing`: set to `blah` to do something

## Known Issues

Calling out known issues can help limit users opening duplicate issues against your extension.

## Release Notes

Users appreciate release notes as you update your extension.

### 1.0.0

Initial release of ...

### 1.0.1

Fixed issue #.

### 1.1.0

Added features X, Y, and Z.

---

## Working with Markdown

**Note:** You can author your README using Visual Studio Code. Here are some useful editor keyboard shortcuts:

- Split the editor (`Cmd+\` on macOS or `Ctrl+\` on Windows and Linux)
- Toggle preview (`Shift+CMD+V` on macOS or `Shift+Ctrl+V` on Windows and Linux)
- Press `Ctrl+Space` (Windows, Linux) or `Cmd+Space` (macOS) to see a list of Markdown snippets

### For more information

- [Visual Studio Code's Markdown Support](http://code.visualstudio.com/docs/languages/markdown)
- [Markdown Syntax Reference](https://help.github.com/articles/markdown-basics/)

**Enjoy!**
