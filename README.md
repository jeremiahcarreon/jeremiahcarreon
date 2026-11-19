```php
<?php

final class Jeremiah extends LifelongLearner
{
    final public const bool CURIOUS = true;     // immutable. tried changing it once. couldn't.
    final public const float LEARNING = INF;

    public function __construct(
        public readonly array $daughters = [1, 2, 3],   // outnumbered, happily
        public readonly string $drives = '4Runner',
        public readonly string $hardware = 'secondhand', // not cheap. resourceful.
    ) {}

    public function handle(Subscription $service): void
    {
        if ($service->costsPerMonth() >= 5) {
            $this->selfHost($service);          // 40 hours to save $5. worth it.
        }
    }

    public function career(): never
    {
        while (self::CURIOUS) {
            $this->askHowItWorks();
            $this->breakIt();
            $this->rebuildIt();
        }
    }
}
```
