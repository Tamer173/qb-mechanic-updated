# qb-mechanic-updated
NUI for Mechanic Shop


NUI for Mechanic Shop

# HOW TO INSTALL

Step 1:

Download and extract the file in [qb] Folder.



Step 2:

add this functions in qb-core/client/functions.lua at Bottom

<!-- Code Start  -->

QBCore.Functions.MathRound = function(value, numDecimalPlaces)
    if numDecimalPlaces then
        local power = 10^numDecimalPlaces
        return math.floor((value * power) + 0.5) / (power)
    else
        return math.floor(value + 0.5)
    end
end

QBCore.Functions.MathGroupDigits = function(value)
    local left,num,right = string.match(value,'^([^%d]*%d)(%d*)(.-)$')

    return left..(num:reverse():gsub('(%d%d%d)','%1' .. _U('locale_digit_grouping_symbol')):reverse())..right
end

QBCore.Functions.MathTrim = function(value)
    if value then
        return (string.gsub(value, "^%s*(.-)%s*$", "%1"))
    else
        return nil
    end
end

<!-- Code End -->


How It Works

You should have mechanic job in order to acces the Menu (You can change the job to allow anyone access the Menu).

To Add More location and Configure Job Open "config.lua"
