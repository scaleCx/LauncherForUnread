add broadcast in com.android.server.telecom.ui.MissedCallNotifierImpl#sendNotificationThroughDefaultDialer:
        Intent newIntent = new Intent(Intent.ACTION_UNREAD_CHANGED);
        newIntent.putExtra(Intent.EXTRA_UNREAD_NUMBER, count);
		newIntent.putExtra(Intent.EXTRA_UNREAD_COMPONENT,
		        new ComponentName(CONTACTS_PACKAGE,CONTACTS_DIALTACTS_ACTIVITY));
	    mContext.sendBroadcast(newIntent);
