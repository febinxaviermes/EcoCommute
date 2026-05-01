# Live Location Tracking - Quick Start Guide

## For Passengers (How to Share Your Location)

### Step 1: Join a Ride
1. Log in to EcoCommute
2. Browse available rides
3. Join a ride that matches your route

### Step 2: Share Your Location
1. Go to the ride details page
2. Click the **"Share My Location"** button (orange button)
3. Read the privacy notice
4. Click **"Start Sharing Location"**
5. When your browser asks for permission, click **"Allow"**

### What You'll See
- ✅ Status: "Active 🟢"
- ✅ Your current coordinates
- ✅ Last update time

### To Stop Sharing
- Click the **"Stop Sharing"** button (red button)
- Your location will immediately stop being shared

### Privacy & Safety
- ✅ Only the ride creator can see your location
- ✅ No location history is stored
- ✅ You can stop sharing at any time
- ✅ Location automatically deleted when ride ends
- ✅ Your exact location is never shown to other passengers

---

## For Ride Creators (How to Track Passengers)

### Step 1: Create a Ride
1. Log in to EcoCommute
2. Click **"Create Ride"**
3. Fill in ride details and submit

### Step 2: View Live Tracking
1. Go to your ride details page
2. Wait for passengers to join
3. Click the **"Track Passenger Locations"** button (blue button)

### What You'll See
- 🗺️ Interactive map with OpenStreetMap
- 📍 Colored markers for each passenger who is sharing their location
- 🟢 "Sharing Location" status for active passengers
- 🔴 "Not Sharing" status for inactive passengers

### Map Features
- **Auto-Refresh**: Map updates every 4 seconds
- **Click Marker**: View passenger details
- **Locate Button**: Center map on specific passenger
- **Auto-Fit**: Map automatically adjusts to show all markers

### Passenger List
- View all passengers who joined your ride
- See real-time sharing status
- See last update timestamp
- Quick access to center map on each passenger

---

## Browser Requirements

### Supported Browsers
- ✅ Chrome 50+
- ✅ Firefox 55+
- ✅ Safari 10+
- ✅ Edge 79+
- ✅ Opera 37+

### Required Permissions
- **Location Access**: Browser must have permission to access location
- **JavaScript**: Must be enabled
- **Cookies**: Required for authentication

### Mobile Devices
- ✅ Works on iOS Safari
- ✅ Works on Android Chrome
- ⚡ Uses less battery than native GPS apps
- 📶 Works on WiFi or cellular data

---

## Troubleshooting

### "Location Permission Denied"
**Problem**: Browser blocked location access
**Solution**: 
1. Click the lock icon in address bar
2. Find "Location" permission
3. Change to "Allow"
4. Refresh the page

### "Location Not Updating"
**Problem**: Location appears frozen
**Solution**:
1. Check your internet connection
2. Make sure you haven't clicked "Stop Sharing"
3. Try refreshing the page
4. Check if browser location services are enabled

### "Map Not Loading"
**Problem**: Tracking page shows blank map
**Solution**:
1. Check your internet connection
2. Disable browser extensions (ad blockers)
3. Try a different browser
4. Clear browser cache

### "Not Authorized" Error
**Problem**: Cannot access tracking page
**Solution**:
- Only the ride creator can track passengers
- Make sure you're logged in
- Make sure you're viewing your own ride

### High Battery Drain
**Problem**: Phone battery draining quickly
**Solution**:
- This is normal for GPS tracking
- Consider plugging in your phone
- Stop sharing when not needed
- Close other apps using location

---

## Frequently Asked Questions

### Q: Can other passengers see my location?
**A:** No, only the ride creator can see your location.

### Q: Is my location history stored?
**A:** No, we only store your current location. As soon as you share a new update, the old one is deleted.

### Q: What happens when the ride ends?
**A:** Your location data is automatically deleted from our servers.

### Q: Can I share my location before the ride starts?
**A:** Yes, you can start sharing anytime after joining a ride.

### Q: Does this work offline?
**A:** No, you need an active internet connection for location updates.

### Q: How accurate is the location?
**A:** Typically within 10-50 meters, depending on your device and environment.

### Q: Does this use a lot of data?
**A:** No, approximately 720 KB per hour (very minimal).

### Q: Can the ride creator see where I've been?
**A:** No, they can only see where you are right now.

### Q: What if I close the browser?
**A:** Location sharing will stop automatically.

### Q: Can I use this while driving?
**A:** Yes, but we recommend having a passenger operate your phone.

---

## Privacy Information

### What We Collect
- ✅ Your current latitude and longitude
- ✅ Timestamp of last update
- ✅ Your consent status (sharing on/off)

### What We DON'T Collect
- ❌ Location history
- ❌ Travel patterns
- ❌ Places you visit
- ❌ Your home or work address (unless you share it)

### Who Can See Your Location
- ✅ The ride creator of rides you've joined
- ❌ Other passengers
- ❌ Other users
- ❌ Public internet

### Data Retention
- While sharing: Location updated every 3-5 seconds
- When stopped: Location immediately deleted
- After ride ends: All location data automatically deleted

### Your Rights
- Right to start/stop sharing anytime
- Right to not share location at all
- Right to delete your account and all data
- Right to know who accessed your location

---

## Technical Details (For Advanced Users)

### How It Works
1. Your browser's Geolocation API (`navigator.geolocation.watchPosition`)
2. Sends coordinates to our server via HTTPS
3. Server stores only the latest position (no history)
4. Ride creator's map polls server every 4 seconds
5. Map updates markers in real-time

### Data Transmission
- **Protocol**: HTTPS (encrypted)
- **Method**: HTTP POST/GET
- **Frequency**: Every 3-5 seconds
- **Payload Size**: ~1 KB per update

### Map Technology
- **Provider**: OpenStreetMap (free, no billing)
- **Library**: Leaflet.js (open source)
- **Updates**: HTTP polling (no WebSockets)

### Security
- CSRF protection enabled
- Authentication required
- Authorization checks on every request
- No API keys exposed to client

---

## Support

If you encounter any issues:
1. Check this guide's troubleshooting section
2. Check your browser console for errors (F12)
3. Contact support with:
   - Browser name and version
   - Device type (mobile/desktop)
   - Screenshot of error
   - Steps to reproduce

---

## Tips for Best Experience

### For Passengers
- ✅ Start sharing location 5-10 minutes before pickup time
- ✅ Keep browser tab open while sharing
- ✅ Charge your phone or use power bank
- ✅ Test location sharing before the actual ride day

### For Ride Creators
- ✅ Ask passengers to start sharing 10 minutes before pickup
- ✅ Use the "Locate" button to quickly find passengers
- ✅ Keep the tracking page open during the ride
- ✅ Refresh if you don't see updates

### General
- ✅ Use on WiFi to save mobile data (if possible)
- ✅ Close other apps to preserve battery
- ✅ Enable "High Accuracy" mode for best results
- ✅ Test in advance to familiarize yourself with the interface

---

## Demo Mode (For Testing)

Want to test the system without actual travel?

### Option 1: Browser Developer Tools
1. Open browser DevTools (F12)
2. Go to "Sensors" or "Location" tab
3. Override location coordinates
4. See marker move on map

### Option 2: Location Spoofing Apps
- Use apps like "Fake GPS" on Android
- Requires USB debugging enabled
- Good for testing different locations

### Option 3: Multiple Devices
- Use one device as passenger
- Another as ride creator
- Walk around to see real-time updates

---

*Last Updated: January 30, 2026*
*EcoCommute - Sustainable Transportation Platform*
