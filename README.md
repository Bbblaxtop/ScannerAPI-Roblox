# Scanner API

##### API for bypassing FE  and scanning backdoors

#

- ⚡Fast Scanning
- 🔍Simple for Scripts
- 😎Easy for Use

#

Copy and Paste
```lua
local function ScannerAPI()
	-- Scanner API
	-- Backdoor Scanner for scripts and etc.

	-- Bypass FE and execute scripts on Server-Side

	-- by salat20
	
	warn("Scanner API | Scanning...")

	for i,v in pairs(game:GetDescendants()) do
		if v:IsA("RemoteEvent") then
			warn("Scanner API | Hooking in "..v.Name.."...")

			v:FireServer("local a = Instance.new'IntValue'; a.Parent = workspace; a.Name = 'ScannerAPI';")

			task.wait(2)

			if workspace.ScannerAPI then
				warn("Scanner API | Hooked "..v.Name.."!")
				_G.ScannerAPIEvent = v
				break
			end
		end
	end
	
	return _G.ScannerAPIEvent
end
```
