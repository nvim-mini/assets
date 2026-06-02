



- Get input from user:

```lua
-- The answer should be two
print(MiniInput.get({ prompt = 'What is one plus one?' }))
```

- `vim.ui.input` implementation:

```lua
-- Precise history which uses past inputs with same metadata
vim.ui.input({ prompt = 'Hello?', scope = 'cursor' }, print)
```

- Configurable view:

```lua
local view_stl = MiniInput.gen_view.uiline({ style = 'statusline' })
MiniInput.get({ prompt = 'Statusline', handlers = { view = view_stl } })

local view_above = MiniInput.gen_view.virtual({ style = 'above' })
MiniInput.get({ prompt = 'Virtual', handlers = { view = view_above } })
```

- Integrates with other 'mini.nvim' modules.
