# final-sales-inventory

## Data persistence

Application data is saved atomically to `data/store.json` after each change, so logging out or restarting the app does not reset inventory, orders, sales, returns, suppliers, or users. Keep the `data` directory on persistent storage when deploying the app; an ephemeral deployment filesystem can still discard files when its host is replaced. When MySQL is configured, it is updated as an additional store; the local JSON file remains the recovery copy.