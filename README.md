
Event:

TriggerEvent('notifications:sendNotification', 2, 'Hello world!', 5000)
For QB Replace:

Go to qb-core\client\functions.lua & search for

function QBCore.Functions.Notify
Delete whole function and replace this

function QBCore.Functions.Notify(text, texttype, length)
    local color = 0
    if texttype == 'success' then color = 3 elseif texttype == 'error' then color = 2 else color = 1 end
    TriggerEvent('notifications:sendNotification', color, text, length or 5000)
end
Colors:

Normal: 1
Error: 2
Warning: 3
Preview
image

Visitor count
