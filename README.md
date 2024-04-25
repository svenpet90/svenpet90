### Hi there 👋

```php
<?php

namespace App\Developer;

#[AsHuman]
final class SvenPetersen extends SymfonyDeveloper implements DeveloperInterface
{
    use Symfony;
    use TYPO3;
    use Twig;
    use Stimulus;
    use HotwiredTurbo;

    public const string FIRST_NAME = 'Sven';
    public const string LAST_NAME = 'Petersen';
    
    public function __construct(
        private \DateTimeImmutable $birthDate = new \DateTimeImmutable('1990-03-04'),
        private string $email = 'sven@hardanders.de',
        private array $currentCompanies = [
            'Dauskonzept GmbH'          => 'Webdeveloper',        // https://dauskonzept.de
            'HardAnders GbR' => 'Founder & Developer', // https://hardanders.de
        ],
        private string $currentCity = 'Schafflund, Germany'
    ) {
    }
    
    public function isOpenForFreelanceWork(): bool
    {
        return true;
    }
}
```
